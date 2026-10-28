# Protocol, signer and node compatibility

Draft 0.4 supplement | Source review 28 October 2026 | Prepared by edgepillar

[Overview](../README.md) | [Architecture](architecture.md) | [Experiment plan](experiment-plan.md) | [Sources](../evidence/sources.md)

This is a source-based capability checklist, not an executed conformance report. The initial product remains one Lightning-paid provider-owned QSR service. Native payer payments and swaps are separate research paths.

## Payment profiles have different contracts

| Profile | Source-supported behavior | Required application boundary |
| --- | --- | --- |
| L402 | A credential and payment preimage authorize restricted service access. Valid credentials may be reused within their scope. | Recover the same paid order or permitted access. Reuse must not create a second fusion job or an unauthorized entitlement. [S10](https://github.com/lightninglabs/L402/blob/592203a95ea297fad6d7e10c6de2d827bfd450b2/protocol-specification.md) |
| x402 exact/lnbtc | The reviewed upfront profile uses `/settle` and prohibits `/verify` for that flow. It uses positive integer millisatoshi strings, signed invoice request binding and an atomic restart-durable replay store. | Follow the chosen profile, invoice issuer and network rules. A generic adapter must not insert a universal verify-then-settle sequence or copy an untyped sats value into the wire amount. [S12](https://github.com/x402-foundation/x402/blob/5847ee5a368130df48bd6ff958e1519de4c41163/specs/schemes/exact/scheme_exact_lnbtc.md) |
| x402 core v2 | The core protocol separates transport, accepted requirements and scheme behavior. | Implement the selected scheme and transport contract; core support does not establish that a custom Zenon network or mechanism is standardized. [S73](https://github.com/x402-foundation/x402/blob/5847ee5a368130df48bd6ff958e1519de4c41163/specs/x402-specification-v2.md) |
| Native Zenon payer PoC | The cited PoC prepares a signed UserSend before facilitator publication and describes an unconsumed staged-signing proposal. | Treat it as a separate experimental adapter. A native transfer signature does not inherently bind an HTTP resource, request body, quote or service-credit policy. Such binding needs an explicit protocol. [S33](https://github.com/edgepillar/zenon-x402-poc/blob/6a0af7d6c96fe770b7c141c44894536f2a543b68/README.md) |

Bind the immutable underlying payment identity to its first order or explicit bounded entitlement. Resource and quote IDs may index that association, but changing them cannot create a second independent claim on the same payment. This application rule must preserve the selected protocol's legitimate retries and credential reuse. An invoice alone still does not identify whether its payer spent held BTC, converted fiat or received an incentive.

For exact/lnbtc, follow the profile's canonical network/payment-hash consumption key. Order or merchant partitioning must not allow independent replay stores to consume the same proof again for one receiver. The application abstraction cannot weaken that normative replay domain.

## Signer capabilities are not interchangeable

| Surface | Reviewed capability | Capability not established by that fact |
| --- | --- | --- |
| Extension `sendAccountBlock` | Human-approved account-block signing and publication. Ferry documents the sign-and-publish boundary. | A detached signed block returned before publication for a facilitator to inspect. [S70](https://github.com/sol-znn/ferry-web/blob/c913cb9e44792b7167a2547fba6b031352939cc7/docs/EXTENSION-WALLET.md) |
| Extension `signMessage` | Message-byte signing with approval. The documented contract rejects inputs whose UTF-8 encoding is exactly 32 bytes. | A raw transaction-hash signing API. Do not bypass the intentional separation by padding or relabeling transaction requests. [S36](https://github.com/sol-znn/syrius-extension/blob/8edb3632014e6dec1206bcd13f876d01c3696947/docs/INTEGRATION.md) |
| SDK staged preparation | Issue #31 records a maintainer-aligned implementation plan. | Delivery or absence of every planned API in an arbitrary source/package version. Match actual exports, installed package and consuming code separately. [S72](https://github.com/digitalSloth/znn-typescript-sdk/issues/31) |
| Provider's unattended signer | A separately proposed, bounded inventory-signing interface in this architecture. | Authority inherited from interactive wallet consent, or an accepted durable signing implementation. |

The paid-fusion product requires provider-side authorization. It does not require customers to sign a native payment. Any future detached-signature interface needs its own source, signature-domain, permission, durable-output and recovery acceptance.

## Node capabilities and deployment evidence

| Source observation | Useful qualification case | Evidence limit |
| --- | --- | --- |
| RPC PR #132 adds per-connection admission limits to the reviewed development work. | Saturated connection, multiple connections, blocked handler, reconnect, deadline and response handling. | A connection-level bound is not an aggregate gateway, byte, HTTP or lifetime bound. Pin the selected source and binary; merge dates do not establish installed behavior. [S66](https://github.com/zenon-network/go-zenon/pull/132) |
| PR #120 preserves pending state across pool rebuild. | Restart/rebuild while the original payment or native job has an unresolved publication outcome. | Pool presence or persistence is not confirmed payment, successful contract processing or finality. [S67](https://github.com/zenon-network/go-zenon/pull/120) |
| The fuzz findings distinguish local decoder failures from tested remote input surfaces, against their reported `60cf7d9` baseline. | If a future snapshot importer crosses this boundary, test length, nil and canonical-validation handling at that actual importer. | The warning is conditional. No observed remote crash in a finite corpus is not a universal safety result or evidence of a current remote exploit. The source document's own commit is distinct from its tested core baseline. [S71](https://github.com/sol-znn/go-zenon-fuzz/blob/166e541ca625cdd503ab16faf94fdefd662f40c4/FINDINGS.md) |

Before any integration, record source revision, binary digest, chain/genesis identity, active rules, SDK and wallet artifacts, transport profile, observation policy and actual outcomes. Preserve failure, unknown and skipped states. Multiple RPC observations can reveal disagreement; they do not authenticate native state values or establish consensus finality.

No adapter, node, wallet, crypto test or payment was executed for this matrix. The [optional interoperability note](interop-research-boundaries.md) has separate future conversion gates.
