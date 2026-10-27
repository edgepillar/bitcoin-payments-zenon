# Possible discussion submission

Draft 0.2 | Source observations through 28 October 2026 | Prepared by edgepillar

[Overview](../README.md) | [Proposal](proposal.md) | [Architecture](architecture.md) | [Experiment plan](experiment-plan.md) | [Sources](../evidence/sources.md)

This text has not been submitted. Repository preparation does not imply contact with Spiral or any maintainer.

## The idea

Test a BTC checkout for an existing Zenon resource service. A customer pays over Lightning; a provider uses its own QSR to supply plasma to the chosen Zenon address. The customer need not acquire QSR for that service. The underlying task may still require a Zenon wallet and other assets.

Zenon has no demonstrated payment advantage over Lightning in this proposal. Its incremental role is a specific service that BTC can purchase. This is a narrow hypothesis about useful spending, not a new payment network or evidence of broad adoption. [S01](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/README.md)

## What it solves

Someone who already needs Zenon resources may prefer paying sats to acquiring QSR or waiting for a constrained sponsor. That preference is unproven. Existing free provision and proof of work could make a paid option unnecessary; both must remain available in the comparison.

Plasma Bot already provides programmatic resource requests. Its roadmap plans QSR or ZNN payments and retains free flows. A BTC option would extend that work subject to maintainer agreement. It is not a claim to have invented resource sponsorship or agent payments. [S04](https://github.com/0x3639/plasma.bot) [S05](https://github.com/0x3639/plasma.bot/blob/main/ROADMAP.md)

## The closest path

Qualify one existing Lightning gateway against immutable orders and durable payment claims. Reuse L402 and paid API tooling. Native fusion separates resource owner and beneficiary, allowing the provider to supply the resource without taking customer keys. [S10](https://github.com/lightninglabs/L402/blob/master/protocol-specification.md) [S11](https://github.com/lightninglabs/aperture) [S06](https://github.com/zenon-network/go-zenon/blob/v0.0.9-alphanet/vm/embedded/implementation/plasma.go)

Reserve inventory before acceptance; journal the original signed native transaction before publication; reconcile uncertain outcomes without another charge or fusion. Confirm the exact contract result and fusion entry, not merely invoice payment or a send hash. Delivery observations retain full node operator trust. [S08](https://github.com/zenon-network/go-zenon/blob/v0.0.9-alphanet/rpc/api/embedded/plasma.go) [S29](https://github.com/edgepillar/zenon-spv/blob/main/docs/verification-contract.md)

Sell a defined allocation under verified chain rules, not guaranteed transaction throughput. Keep protected paid allocations out of early recycling. Upfront payment creates a provider obligation; compensation is separately specified. Canceling a settled Lightning invoice is not a refund. No BTC bridge, swap, ZVM escrow or new activation is needed for this service. [S17](https://lightning.engineering/api-docs/api/lnd/invoices/cancel-invoice/)

## Who could make it happen

The required roles are a willing resource operator, a Lightning integration developer and an independent security and measurement reviewer. Their participation and implementation costs remain open. I would ask Spiral to critique the use case and outcomes and, if useful, suggest a reviewer. No endorsement, funding or partnership is assumed.

## How we would know it is working

Start with ten prospective customer interviews and up to three operator interviews over two weeks. Prototype only if a concrete need at an actual offered price survives adequate free alternatives. These are proposed discovery limits, not demand evidence.

Before real value, test response loss, concurrent claims, database and publication uncertainty, wrong beneficiaries, contract rejection, inventory recycling and compensation failure. Require no duplicate accepted claim, native authorization, budget breach or violation of the sold condition in the declared corpus. Publish failures and skipped cases.

After separate acceptance, propose a 30 day feasibility study with two providers and up to 60 eligible participants. Randomize whether the BTC option is offered while keeping existing alternatives available. Compare completion of the already intended task by a fixed deadline. Report BTC uptake separately: payment substitution need not create additional activity. A separate automation test holds the Lightning rail and service terms fixed.

Count distinct unsubsidized BTC customers, observed deliveries, net revenue, all in cost and unresolved liabilities. Report conversion over everyone eligible. Measure renewal only when a customer genuinely needs renewal within the window. A proposed commercial continuation filter is ten distinct paying customers across both providers and positive contribution margin under disclosed capital and support assumptions. This only justifies further study; the pilot is not powered to prove superiority or broad adoption.

Stop if adequate free routes dominate, demand is absent or economics fail. Retain the reusable Lightning recovery work and publish the negative finding. The full draft defines the architecture, fault matrix and source boundaries. This is a focused experiment proposal using Spiral's fields, and remains unsubmitted. [S03](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/.github/ISSUE_TEMPLATE/moonshot-idea.yml)
