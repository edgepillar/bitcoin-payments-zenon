# Optional interoperability research boundaries

Draft 0.4 supplement | Source review 28 October 2026 | Prepared by edgepillar

[Overview](../README.md) | [Architecture](architecture.md) | [Experiment plan](experiment-plan.md) | [Sources](../evidence/sources.md)

This note records optional conversion research. The first proposed product remains a Lightning payment for provider-owned QSR fusion. It needs no customer native transfer, asset swap, BTC representation, PTLC activation or ZVM contract. Demand and operator acceptance remain prerequisites for implementation priority.

## Keep payment and conversion mechanisms distinct

| Mechanism | Reviewed role and limit |
| --- | --- |
| Lightning checkout | Pays for the resource service. Service delivery and compensation remain provider obligations; a settled invoice is not proof of BTC funding source. |
| Ferry HTLC construction | Bitcoin P2SH and Zenon native HTLC legs use a shared secret. This is separate from Lightning and does not require the future PTLC feature. The test plan retains refund and recovery acceptance gaps. |
| Zenon PTLC | A conditional native contract and client-protocol research input. It does not itself create cross-chain liquidity, a Lightning channel or guaranteed service delivery. |
| Treasury conversion | A separately specified inventory operation. Fast provider or LP payout before swap completion can introduce credit exposure; it is not request-scale atomic settlement. |

Ferry's [security model](https://github.com/sol-znn/ferry-web/blob/c913cb9e44792b7167a2547fba6b031352939cc7/docs/SECURITY.md) and [testing plan](https://github.com/sol-znn/ferry-web/blob/c913cb9e44792b7167a2547fba6b031352939cc7/docs/TESTING.md) are source observations, not this proposal's independent acceptance of the client or deployment. Small transaction value does not resolve missing refund evidence.

## Reclaim authorization added after the original PTLC work

[PR #216](https://github.com/zenon-network/go-zenon/pull/216) merged into `dev` on 24 October 2026 at `b436efe5fe9a3663851b15ea44cbcf2235f5bf73`. It adds optional reclaim-lock methods. For such an entry, reclaim requires its creator, expiry eligibility and a valid signature under the stored reclaim key; ordinary unsigned reclaim is refused. A creator unable to obtain a valid signature cannot use an unsigned fallback. Checking the needed authorization before funding is a client safety requirement, not a contract rule about when the signature was obtained. [Implementation](https://github.com/zenon-network/go-zenon/blob/b436efe5fe9a3663851b15ea44cbcf2235f5bf73/vm/embedded/implementation/ptlc.go)

The reclaim message binds chain/contract context and immutable entry terms rather than the creating transaction ID. Distinguish its serialized fields from the stored reclaim key used for verification: the key bytes are not another serialized field in that message. Identical terms under the same key can reuse an authorization. Require fresh keys per economic swap **and** durable funding-intent uniqueness; fresh keys alone cannot prevent accidentally funding an intent twice. Implementations must follow the exact serialization and domain in the [message definition](https://github.com/zenon-network/go-zenon/blob/b436efe5fe9a3663851b15ea44cbcf2235f5bf73/vm/embedded/definition/ptlc.go), not reconstruct an informal list of fields.

Signature-bearing reclaim can support particular adaptor-share fairness constructions. It does not establish fair exchange for every swap, a completed Zenon-Monero system or automatic BTC conversion.

## Compatibility and evidence gates

The additional methods use the PTLC spork. A network already running PTLC needs coordinated node compatibility before the new methods are used; an existing activation flag does not demonstrate that every relevant node understands them. The cited development sources report mainnet inactivity. This review did not independently query a live network.

A development merge, release source, downloaded binary, active chain rules, client compatibility and recovery acceptance are separate evidence. Freeze the exact selected software and chain profile before any future experiment. Do not infer binary contents or deployment from merge dates. No funded operation is authorized by this note.

## Proposed future fault vectors

These cases have not been executed here.

| ID | Case and expected acceptance evidence |
| --- | --- |
| IR01 | Change each signed term or domain independently; the original authorization must not validate the changed transcript. |
| IR02 | Substitute the stored reclaim key; verification must use that key and reject an incompatible authorization. |
| IR03 | Repeat identical terms with a reused key; document the authorization-reuse behavior and demonstrate client rejection of unsafe key reuse before another funding intent. |
| IR04 | Submit the same economic funding intent concurrently, after restart and with fresh keys; no second independent funding authority may be created. |
| IR05 | Remove or corrupt the required pre-obtained authorization; the client must refuse funding, without assuming the contract enforces this timing requirement. |
| IR06 | Exercise unlock/reclaim domains, expiry boundaries and late witness publication; rejection must not be mistaken for witness secrecy. |
| IR07 | Lose watcher, RPC or coordinator responses between both-chain claim/refund steps; preserve original identities and unresolved outcomes without replacement funding. |
| IR08 | Mix spork-off and incompatible already-active node versions; refuse the experiment before funding until the selected compatibility gate is established. |

Public results should use sanitized aggregates and agreed role aliases. Keep keys, preimages, payment-to-address linkage and raw recovery journals out of publication. No native tests, cryptographic executions, swaps or live payments were performed for this supplement.
