# Experiment plan and acceptance evidence

Draft 0.2 | Source observations through 28 October 2026 | Prepared by edgepillar

[Overview](../README.md) | [Proposal](proposal.md) | [Architecture](architecture.md) | [Experiment plan](experiment-plan.md) | [Sources](../evidence/sources.md)

## First establish a reason to pay

Proposed discovery cap: ten prospective customer interviews and up to three provider interviews over two weeks. Ask for an already desired task, the best available free or native path, its observed friction, and a response to a concrete provider price and service condition. Interview interest is not a payment. Proceed to a prototype only if at least three prospective customers identify the need at that offered price and two independent providers can state deliverable inventory and terms. These are proposed investment filters, not observed demand or statistical evidence.

If free sponsorship or proof of work meets the requirement with acceptable delay and reliability, stop the commercial hypothesis. Do not disable an adequate free option to create apparent demand. If discovery reveals a different useful service, rewrite the delivery contract and comparator before coding.

## Separate the causes of any improvement

| Experiment | What stays comparable | What its result can establish |
| --- | --- | --- |
| Payment option | Give all eligible participants the same underlying service and access to existing alternatives. Randomize whether the BTC option is offered, with crossover recorded. | Compare completion of the already intended task by a fixed deadline. BTC uptake is a separate commercial observation, not proof of additional activity. |
| Automation ablation | Hold the Lightning payment, quote terms and inventory policy fixed. Compare assisted manual native fulfillment with the proposed job worker, in a separate test. | Effect of automation and recovery. Attribute improvements to the adapter, not to a consensus property. |
| Generic paid API control | Use the same payment and journal against an ordinary stored result service that needs no native resource action. | Which tooling is reusable without Zenon. Any claimed generic payment improvement must survive this control. |

Do not force participants to pay or withhold a needed free service. A randomized offer estimates availability of the checkout, including choices not to use it. Report intention to treat, crossover, prior BTC and native asset holdings, support and free capacity availability. Native asset conversion and voluntary route selection must not be pooled into a claim of causal payment improvement.

The primary comparative outcome is completion of the already intended task by a prespecified deadline over everyone assigned to each arm. Define that task and its acceptable evidence before enrollment; resource delivery and task completion remain separate. Report total task activity and payment method share. A shift from native payment to BTC can show customer preference without creating additional economic activity. A crypto native sample cannot establish mainstream merchant adoption.

## A bounded feasibility pilot

After engineering and operator acceptance, propose a 30 day window with two independent providers and up to 60 eligible participants who already have a relevant task. These planning values are not a powered study. Freeze enrollment rules, assignment, denominators, price, workload, observation window and analysis before outcomes. An operator must separately set monetary, inventory and compensation caps before any live step; this draft authorizes no live funds.

Primary commercial observation: distinct customers who make an unsubsidized BTC payment and receive the declared resource service, plus net BTC revenue after refunds and all in cost per completed order. Report purchase conversion over every eligible enrolled participant, not only those who reach checkout. Count one order per intent; retries retain its identity. Separate trials, incentives, operator accounts, swaps, credits and QSR movements from customer BTC payments.

Retention is secondary and must fit the resource term. Report repeat purchases only among customers whose delivered service could genuinely need renewal within the window. An unexpired allocation is not failed retention. Record the eligible renewal denominator; fewer than ten eligible customers leaves renewal inconclusive. Any optional evidence that a provider spends its BTC earnings elsewhere is a separate descriptive outcome, not proof of a closed economic loop.

Proposed commercial continuation filter: at least ten distinct unsubsidized customers across both providers, with positive contribution margin after routing, compensation, inventory capital, infrastructure and measured support costs under disclosed assumptions. Report each provider separately; do not hide a loss behind the other provider. This filter only justifies further study. If adequate free options dominate or costs exceed willingness to pay, stop the paid branch and retain the reusable Lightning findings.

Report raw counts and participant level intervals where appropriate; with two providers, provider effects are descriptive. A small pilot cannot establish production reliability, statistical superiority or broad adoption. Design a larger replication from the pilot baseline and a prespecified worthwhile effect before making those claims.

## Metrics and bounded failure qualification

| Measure | Definition and decision use |
| --- | --- |
| Demand and access | Eligible participants, offers shown, existing free options, BTC purchasers and observed deliveries. Report random assignment and crossover; disclose dependence on the existing Zenon community. |
| Fulfillment | Payment to successful contract outcome and declared service condition. Report p50, p95, unresolved age and the separate time to a real customer task. Do not equate invoice settlement, send acceptance and delivery. |
| Unit economics | Net sats minus routing, compensation, support, infrastructure and allocated capital cost. Record QSR quantity, valuation, utilization and actual lock duration. Returning principal does not erase capital or asset price exposure. |
| Renewal | Repeat orders divided by customers whose service condition creates a genuine renewal opportunity in the observation window. Report censoring and missing follow up. |
| Safety and liabilities | Unique accepted payment claim, one authorized native job, reserved inventory and separately tracked compensation. No duplicate debit, native execution authorization, early recycling or budget breach is permitted in the stated corpus. |

First run local and integrated test environments using an exact manifest of node and wallet builds, genesis, active rules, SDK, gateway, database schema, workload and actual command outcomes. The proposed deterministic corpus repeats each applicable failure at least 20 times, including one worker and three gateway replicas. Also run a 60 minute workload at twice the intended pilot peak. These are bounded qualification targets, not tests already run or proof of production capacity.

| Injected failure | Required outcome |
| --- | --- |
| Paid response loss and replay | Recover the same order and result. Replicas and restarts cannot create another accepted claim or job. Respect the selected protocol's legitimate credential reuse. |
| Wrong or changed order | Wrong beneficiary, owner, amount, chain, genesis, expired quote or mutated terms cannot obtain delivery authority. Never identify delivery solely from an aggregate balance. |
| Late payment after expiry | Record any verified payment as a liability even if the quote or inventory reservation expired. Reconcile the original order; do not discard the payment, silently reprice it or authorize another charge. |
| Database or native publication uncertainty | At each commit boundary preserve original signed bytes, hash and owner. Reconcile before any new action; an unknown outcome is not permission to sign again. |
| Send accepted but contract fails | A rejected or absent contract result remains undelivered or unresolved under the stated policy. Do not issue a successful service receipt from the send alone. |
| Inventory exhaustion or recycling | Reservations fail before payment acceptance where possible. Protected paid allocations cannot be selected for early recycling. A cancel request is not immediately spendable inventory. |
| Signer or account chain conflict | Only the quoted Fuse operation is allowed. Per owner serialization and bounded signing authority hold under concurrent orders and restarts. |
| Compensation failure | Authenticate the original customer's remedy and record its payment identity. A lost refund response cannot authorize another payout or a false completed refund. |
| Observation disagreement or outage | Retain a visible unresolved state and the original evidence. Independent observations do not silently become a consensus or state proof. |

Stop the affected test on an unexplained debit, wrong beneficiary, unjournaled signature, duplicate authorization, violated sold condition or unresolved real value incident. Preserve failure evidence privately and publish sanitized outcomes only after review. A later pass does not erase a failure. Expansion needs an independent review of the cause and new bounded acceptance.
