# Experiment plan and acceptance evidence

Draft 0.3 | Source review 28 October 2026 | Prepared by edgepillar

[Overview](../README.md) | [Proposal](proposal.md) | [Architecture](architecture.md) | [Experiment plan](experiment-plan.md) | [Sources](../evidence/sources.md)

## First establish a reason to pay

Proposed discovery cap: ten prospective customer interviews and up to three provider interviews over two weeks, using no more than three person-days. Ask for an already desired task, the best available free or native path, its observed friction, and a response to a concrete provider price and service condition. Include people who tried a free route successfully and people who declined the proposed service. Interview interest is not a payment. Proceed to a prototype only if at least three prospective customers identify the need at that offered price and two independent providers can state deliverable inventory and terms. These are proposed investment filters, not observed demand or statistical evidence.

If free sponsorship or proof of work meets the requirement with acceptable delay and reliability, stop the commercial hypothesis. Do not disable an adequate free option to create apparent demand. If discovery reveals a different useful service, rewrite the delivery contract and comparator before coding.

## Separate the causes of any improvement

| Experiment | What stays comparable | What its result can establish |
| --- | --- | --- |
| Payment option | Give all eligible participants the same underlying service and access to existing alternatives. Randomize whether the BTC option is offered, with crossover recorded. | Compare completion of the already intended task by a fixed deadline. BTC uptake is a separate commercial observation, not proof of additional activity. |
| Automation ablation | Hold the Lightning payment, quote terms and inventory policy fixed. Compare assisted manual native fulfillment with the proposed job worker, in a separate test. | Effect of automation and recovery. Attribute improvements to the adapter, not to a consensus property. |
| Generic paid API control | Use the same payment and journal against an ordinary stored result service that needs no native resource action. | Which tooling is reusable without Zenon. Any claimed generic payment improvement must survive this control. |

Do not force participants to pay or withhold a needed free service. A randomized offer estimates availability of the checkout, including choices not to use it. Report intention to treat, crossover, prior BTC and native asset holdings, support and free capacity availability. Native asset conversion and voluntary route selection must not be pooled into a claim of causal payment improvement.

The primary comparative outcome is completion of the already intended task by a prespecified deadline over everyone assigned to each arm. Define that task and its acceptable evidence before enrollment; resource delivery and task completion remain separate. Block assignment by provider and task class, record free-service capacity at the time of the offer and prevent inventory promised to one arm from silently exhausting the other's capacity. If meaningful interference cannot be controlled or described, treat the comparison as descriptive rather than causal.

Freeze the analysis and its commit hash before enrollment. Count missing task completion evidence as not established for the primary analysis, then report missingness and a sensitivity analysis. Do not exclude a participant because payment failed, a free route was chosen or the result is inconvenient. With only two providers, do not claim population-level provider or cluster effects.

Report total task activity and payment method share. A shift from native payment to BTC can show customer preference without creating additional economic activity. A crypto native sample cannot establish mainstream merchant adoption.

## Distinguish bitcoin spending from a Lightning rail

A settled BTC-denominated Lightning invoice does not establish that the customer spent a previously held bitcoin balance. A dollar wallet may have funded it. Spiral explicitly separates those outcomes. Ask only for a voluntary funding category: existing BTC balance, fiat conversion at payment, third-party incentive, or unknown. Do not collect identity, wallet balances, screenshots or public account-linkage proofs to classify it. [S01](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/README.md)

Report settled Lightning orders and their value separately from self-reported unsubsidized BTC-funded orders. Self-report is not independent proof; report unknown funding as unknown and show a lower identified count plus an upper bound including unknown cases. Exclude known incentives and operator-funded accounts from the unsubsidized numerator. Separate a share of all completed service orders, including free orders, from a share of paid orders; publish each denominator and never combine the two.

An enrollment pseudonym is not proof of a distinct human. Prespecify minimal deduplication rules and disclose Sybil and self-report limits. Report distinct eligible enrollment units that purchased and received the service, not verified natural persons. Public datasets must not contain wallet addresses, invoice identifiers, exact transaction times or stable hashes that reconnect them.

## A bounded feasibility pilot

After engineering and operator acceptance, propose a 30 day window with two independent providers and up to 60 eligible participants who already have a relevant task. These planning values are not a powered study. Freeze enrollment rules, assignment, denominators, price, workload, observation window and analysis before outcomes. An operator must separately set monetary, inventory and compensation caps before any live step; this draft authorizes no live funds.

Primary commercial observation: eligible enrollment units that report an unsubsidized BTC-funded payment and receive the declared resource service, together with separately reported settled Lightning volume, funding uncertainty, net BTC revenue after refunds and all in cost per completed order. Report purchase conversion over every eligible enrolled participant, not only those who reach checkout. Count one order per intent; retries retain its identity. Separate trials, incentives, operator accounts, swaps, credits and QSR movements from customer payments.

Retention is secondary and must fit the resource term. Report repeat purchases only among customers whose delivered service could genuinely need renewal within the window. An unexpired allocation is not failed retention. Record the eligible renewal denominator; fewer than ten eligible customers leaves renewal inconclusive. Any optional evidence that a provider spends its BTC earnings elsewhere is a separate descriptive outcome, not proof of a closed economic loop.

Proposed commercial continuation filter: at least ten eligible paying enrollment units across both providers that report unsubsidized BTC funding, with positive contribution margin after payment operations, compensation, inventory capital, infrastructure and measured support costs under disclosed assumptions. Unknown funding cannot satisfy this filter. This does not prove ten different humans. Report each provider separately; do not hide a loss behind the other provider. This filter only justifies further study. If adequate free options dominate or costs exceed willingness to pay, stop the paid branch and retain the reusable Lightning findings.

Report raw counts and participant level intervals where appropriate; with two providers, provider effects are descriptive. A small pilot cannot establish production reliability, statistical superiority or broad adoption. Design a larger replication from the pilot baseline and a prespecified worthwhile effect before making those claims.

## Metrics and bounded failure qualification

| Measure | Definition and decision use |
| --- | --- |
| Demand and access | Eligible participants, offers shown, existing free options, BTC purchasers and observed deliveries. Report random assignment and crossover; disclose dependence on the existing Zenon community. |
| Fulfillment | Payment to successful contract outcome and declared service condition. Report the sample size, observed durations, descriptive p50/p95 and unresolved age, plus the separate time to a real customer task. Small-sample percentiles are not reliability guarantees. Do not equate invoice settlement, send acceptance and delivery. |
| Unit economics | Customer receipts minus actual provider payment-operation costs, compensation, support, infrastructure and allocated capital cost. Record QSR quantity, valuation, utilization, actual lock duration, incoming liquidity and rebalancing. Assign routing fees to whoever actually paid them; do not charge the same cost twice. Returning principal does not erase capital or asset price exposure. |
| Renewal | Repeat orders divided by enrollment units with a genuine renewal opportunity in the observation window. Native cancellation eligibility alone does not end the allocation and is not proof that renewal was needed. Report censoring and missing follow up. |
| Safety and liabilities | Unique accepted payment claim, one authorized native job, reserved inventory and separately tracked compensation. No duplicate debit, native execution authorization, early recycling or budget breach is permitted in the stated corpus. |

First run local and integrated test environments using an exact manifest of node and wallet builds, genesis, active rules, SDK, gateway, database schema, workload and actual command outcomes. The proposed deterministic corpus repeats each applicable failure at least 20 times, including one worker and three gateway replicas. Also run a 60 minute workload at twice the intended pilot peak. These are bounded qualification targets, not tests already run or proof of production capacity.

| Injected failure | Required outcome |
| --- | --- |
| Paid response loss and replay | Recover the same order and result. Replicas and restarts cannot create another accepted claim or job. Respect the selected protocol's legitimate credential reuse. |
| Same payment under a different quote or resource | Submit one immutable payment identity with changed quote/resource metadata, including concurrent requests and restart. It cannot create a second independent entitlement or native authorization. Recovery of the original order and legitimate bounded L402 access must still work. |
| Wrong or changed order | Wrong beneficiary, owner, amount, chain, genesis, expired quote or mutated terms cannot obtain delivery authority. Never identify delivery solely from an aggregate balance. |
| Late payment after expiry | Record any verified payment as a liability even if the quote or inventory reservation expired. Reconcile the original order; do not discard the payment, silently reprice it or authorize another charge. |
| Database or native publication uncertainty | At each commit boundary preserve original signed bytes, hash and owner. Reconcile before any new action; an unknown outcome is not permission to sign again. |
| Send accepted but contract fails | A rejected or absent contract result remains undelivered or unresolved under the stated policy. Do not issue a successful service receipt from the send alone. |
| Inventory exhaustion or recycling | Reservations fail before payment acceptance where possible. Protected paid allocations cannot be selected for early recycling. A cancel request is not immediately spendable inventory. |
| Signer or account chain conflict | Only the quoted Fuse operation is allowed. Per owner serialization and bounded signing authority hold under concurrent orders and restarts. |
| Signer response loss | Recover the durably recorded original signed payload. A timeout or crash after signing cannot authorize a replacement signature or account-chain operation. If the signer cannot recover it, hold the account and stop. |
| Paged or stale fusion entries | Traverse the declared bounded owner-indexed lookup and retain its observation anchor. A missing page, wrong owner or stale endpoint cannot authorize a replacement job. |
| Payment evidence mismatch | Reject a wrong issuer, network, amount, payment hash or order restriction. Repeated valid L402 access recovers the original order. Funding category remains a measurement field, never payment authorization. |
| Compensation failure | Authenticate the original customer's remedy and record its payment identity. A lost refund response cannot authorize another payout or a false completed refund. |
| Observation disagreement or outage | Retain a visible unresolved state and the original evidence. Independent observations do not silently become a consensus or state proof. |

Stop the affected test on an unexplained debit, wrong beneficiary, unjournaled signature, duplicate authorization, violated sold condition or unresolved real value incident. Preserve failure evidence privately and publish sanitized outcomes only after review. A later pass does not erase a failure. Expansion needs an independent review of the cause and new bounded acceptance.

The [compatibility matrix](compatibility-matrix.md) identifies scheme, signer and node boundaries to freeze before execution. The eight [optional interoperability vectors](interop-research-boundaries.md) are separate future research and have not been executed. Neither set adds a swap or native customer-payment dependency to this experiment.
