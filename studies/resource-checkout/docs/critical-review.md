# Critical review of the proposal

Draft 0.3 | Source review 28 October 2026 | Prepared by edgepillar

[Overview](../README.md) | [Proposal](proposal.md) | [Architecture](architecture.md) | [Experiment plan](experiment-plan.md) | [Sources](../evidence/sources.md)

This is an independent critical assessment, not feedback received from Spiral.

## Overall judgment

Version 0.1 was careful about evidence but did not establish why Zenon belonged in the minimum product. Its generic service economy mostly described a Lightning application. Its more concrete native escrow changed the asset and trust model, which made it a poor test of bitcoin payment value. I would not present that version as a demonstrated adoption solution.

Version 0.2 narrowed the proposal to a BTC checkout for an existing Zenon resource provider. Version 0.3 retains that narrow scope while correcting the delivery term, funding classification, source provenance and privacy limits. Commercial demand is still unknown. The correct decision is bounded discovery, with implementation priority, real value deployment and superiority claims held back until separate evidence exists. This remains a small testbed rather than a demonstrated moonshot.

## 1 The original comparison did not justify another chain

**Severity: blocking for the original thesis.**

Objection: paid APIs, session accounting, agent budgets and recoverable service requests can be implemented around Lightning. L402 and Aperture are existing work, and LND exposes conditional invoice primitives. These are stronger baselines than an unspecified provider ledger. The fact that one x402 scheme is upfront does not mean the entire Lightning ecosystem lacks conditional payment. [S10](https://github.com/lightninglabs/L402/blob/592203a95ea297fad6d7e10c6de2d827bfd450b2/protocol-specification.md) [S11](https://github.com/lightninglabs/aperture/blob/f6d91e78f22b445fea8e112f30172e5ea8b6cff3/README.md) [S15](https://lightning.engineering/api-docs/api/lnd/invoices/add-hold-invoice/)

Correction: the revised draft explicitly grants the generic payment role to Lightning and removes generic escrow as the principal reason to add Zenon. Zenon's concrete role is delivering a native resource to an independently chosen beneficiary. This complements Lightning; it does not establish that Zenon moves BTC better.

Remaining question: does anyone want that native service enough to pay BTC for it?

## 2 The old escrow did not measure a bitcoin benefit

**Severity: blocking for the old flagship experiment.**

Objection: the acknowledgment and timeout design allowed a customer to receive useful work and then force a refund by withholding acknowledgment. Its native asset cohort could at most test that workflow and its trust model. It could not establish better BTC service completion or adoption. Committee asset custody also survived application escrow logic. [S40](https://github.com/Zenoglyphs-VM/zvm-docs/blob/35c5be8a59059a9e1f3aab40c980ef6cd18cf0be/operations/COMMITTEE.md)

Correction: remove the proposed ZVM reservation from the first product. No new escrow, peg, oracle or consensus change is needed for the resource checkout. Future swap or application contract studies must establish their own customer need, adversarial economics and acceptance.

## 3 Existing sponsorship and its roadmap change the novelty claim

**Severity: major omission in the original research framing.**

Objection: Plasma Bot already offers a resource service and agent API. Its roadmap also plans native paid access while retaining free flows. A new service platform would duplicate existing work, and a paid hypothesis must survive the free alternative. The first draft omitted this particularly relevant implementation. [S04](https://github.com/0x3639/plasma.bot/blob/ada5a03a458c17c18083fcc099276248e8f611fe/README.md) [S05](https://github.com/0x3639/plasma.bot/blob/ada5a03a458c17c18083fcc099276248e8f611fe/ROADMAP.md)

Correction: propose an optional BTC adapter to the existing service, with overlap and maintainer checks before coding. Do not claim first invention, existing BTC support or a deployed paid product. Do not manufacture scarcity by disabling adequate free access.

## 4 Customer benefit needed a precise delivery object

**Severity: major.**

Objection: generic terms such as coordination, conditional service and session funding hid the actual thing purchased. A claimed number of transactions would depend on workload and the active resource model. A universal wall clock lease cannot be inferred from one source constant.

Correction: quote a defined allocation, beneficiary and enforceable minimum service condition under pinned actual rules. The native implementation separates owner and beneficiary and restricts cancellation by the entry's conditions. The customer avoids acquiring QSR for this service, while still potentially needing a wallet or assets for the task. [S06](https://github.com/zenon-network/go-zenon/blob/bb39e31c608dc397a91b98b21b096bca99a9f4d6/vm/embedded/implementation/plasma.go) [S09](https://github.com/zenon-network/go-zenon/blob/bb39e31c608dc397a91b98b21b096bca99a9f4d6/vm/constants/embedded.go)

Remaining question: is removing this acquisition step worth more than its provider cost when free provision is available?

## 5 Payment success and service delivery still had an unclosed gap

**Severity: major engineering boundary.**

Objection: a paid invoice or accepted native send is not the successful execution of the purchased resource service. The RPC's entry listing is owner indexed, and a beneficiary aggregate can include unrelated resources. An uncertain compensation payment has the same duplicate payout risk as an uncertain purchase. [S08](https://github.com/zenon-network/go-zenon/blob/bb39e31c608dc397a91b98b21b096bca99a9f4d6/rpc/api/embedded/plasma.go)

Correction: bind order identity to exact provider and entry, inspect actual contract processing and service conditions, and separate payment, job, delivery and compensation states. Preserve signed bytes and hash before publication. Unknown outcomes cannot authorize another native execution or payout.

## 6 The proposed inventory business had no priced service guarantee

**Severity: major commercial and safety issue.**

Objection: automatic recycling suitable for a free sponsor can conflict with sold resource conditions. Recoverable QSR principal is still capital with lock duration, utilization and price exposure; it is not free infrastructure. Fees alone are not the relevant economic denominator.

Correction: review the documented recycling policy before reusing it for paid orders, reserve inventory atomically, and prohibit early recycling of protected entries. Model net revenue after capital, infrastructure, support and compensation, with actual observed duration and disclosed valuation. Do not assume an accepted cancellation immediately returns spendable inventory. [S04](https://github.com/0x3639/plasma.bot/blob/ada5a03a458c17c18083fcc099276248e8f611fe/README.md) [S06](https://github.com/zenon-network/go-zenon/blob/bb39e31c608dc397a91b98b21b096bca99a9f4d6/vm/embedded/implementation/plasma.go)

## 7 The original experiment mixed causal questions and arbitrary filters

**Severity: major measurement weakness.**

Objection: a native asset comparison, an automation comparison and BTC adoption are different questions. A 20 percent cost reduction or 10 percentage point completion gain could reward a convenient outcome rather than test the principal claim. A 100 participant feasibility sample did not justify superiority or a 5 point retention noninferiority conclusion. Buying an allocation that remains useful for weeks also makes three separate purchase days an unsuitable universal retention rule.

Correction: separate randomized BTC option availability from a same rail automation test. Keep free alternatives accessible and preserve original assignment. Compare intended task completion by a fixed deadline and report payment method share separately. Switching existing activity to BTC is different from creating additional activity, and a crypto native sample does not establish mainstream merchant adoption. Use conversion over all eligible participants, renewal only when eligible and explicitly proposed commercial filters. A larger replication needs a powered plan based on its own worthwhile effect. The proposed counts in version 0.2 are planning filters, not scientific significance thresholds.

## 8 Ecosystem progress was too prominent relative to the dependency case

**Severity: substantial editorial weakness.**

Objection: a long inventory can read as a technology pitch even when every caveat is accurate. Merged PTLC, candidate state roots, Dynamic Plasma and a broad EVM app family do not demonstrate additional BTC customers. They also enlarge the apparent implementation burden.

Correction: put recent ecosystem work in an appendix with an explicit role or reason for deferral. The first service uses qualified existing fusion and a Lightning gateway. Keep state value proof and activation limits explicit. Public native x402 pending qualification remains incomplete; it is not silently promoted into the new BTC adapter. [S29](https://github.com/edgepillar/zenon-spv/blob/2776e2b38847bc7b7bc338cb750663b83c92a04d/docs/verification-contract.md) [S19](https://github.com/zenon-network/go-zenon/blob/77ba9c7ee8c881e90911946756cdb67d8b586043/common/types/spork.go) [S34](https://github.com/edgepillar/zenon-x402-poc/blob/6a0af7d6c96fe770b7c141c44894536f2a543b68/docs/P1_NATIVE_V4_PENDING_LOCAL_QUALIFICATION.md)

## 9 The trust claim needed to survive the full transaction

**Severity: major.**

Objection: noncustodial keys or a native contract do not make upfront BTC payment fair exchange for resource delivery. Full node observations have operator trust. A hold invoice is not automatically compatible with an upfront scheme, and invoice cancellation does not refund a settled payment. [S12](https://github.com/x402-foundation/x402/blob/5847ee5a368130df48bd6ff958e1519de4c41163/specs/schemes/exact/scheme_exact_lnbtc.md) [S17](https://lightning.engineering/api-docs/api/lnd/invoices/cancel-invoice/)

Correction: use plain provider delivery and compensation terms. Keep any hold invoice experiment separately specified and measure its provider exposure and liquidity. Make no trustless BTC escrow, inherited bitcoin security, anonymity or guaranteed throughput claim.

## 10 The ask and implementation scope were larger than the evidence supported

**Severity: editorial and resource allocation concern.**

Objection: a service network, multiple adapters, new escrow, swaps and proof work are too many dependencies before there is a customer. A reviewer needs a small result and a clear stop condition, not a comprehensive platform roadmap.

Correction: ask Spiral to critique one use case and its measurements. Deliver discovery first, one adapter only if justified, and a reusable failure corpus even if the paid branch stops. Record maintainer agreement, exact source pins, operator inventory caps and independent acceptance as unresolved prerequisites. Commit no person's time, funding or production role. [S02](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/CONTRIBUTING.md)

## 11 Lightning routing was not enough evidence of bitcoin spending

**Severity: major measurement correction for Draft 0.2.**

Spiral separates spending bitcoin from using Lightning to route value funded in dollars. A settled invoice establishes the rail, not the customer's prior funding asset. Draft 0.3 therefore records funding categories voluntarily, reports self-report and Sybil limits, and preserves an unknown category. The ten-unit commercial filter requires reported unsubsidized BTC funding. No identity or wallet-balance collection is introduced to overstate certainty. [S01](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/README.md)

## 12 A stronger service term and signer contract were still needed

**Severity: major specification correction for Draft 0.2.**

The reviewed native `expirationHeight` is cancellation eligibility, not an automatic end or a configurable lease. A longer provider promise needs a separate contractual label. The order also needs distinct invoice, quote and delivery deadlines, an exact owner-and-send-hash delivery identity and a signer response-loss case that recovers original bytes. These are proposed acceptance requirements, not behavior established by a diagram or a database uniqueness constraint. [S06](https://github.com/zenon-network/go-zenon/blob/bb39e31c608dc397a91b98b21b096bca99a9f4d6/vm/embedded/implementation/plasma.go) [S08](https://github.com/zenon-network/go-zenon/blob/bb39e31c608dc397a91b98b21b096bca99a9f4d6/rpc/api/embedded/plasma.go)

## 13 Source breadth was not the same as source specificity

**Severity: substantial evidence correction for Draft 0.2.**

Moving repository links hid the exact file used for a conclusion. A release's target revision, a fork's default README and a working implementation branch are different evidence. Draft 0.3 pins reviewed GitHub files, records PR and release metadata, narrows repository-only observations and marks the Word export as historical. Recent ecosystem activity remains context rather than evidence of demand or activation. The [publication review](../evidence/publication-review.md) records the correction scope.

## What is stronger now

The proposal states what Zenon adds, what Lightning already does, what a customer purchases, which existing project to extend, and the free service that may falsify the business. It has an actual order and inventory architecture, a narrower trust claim, a fairer comparator and explicit negative outcomes. These corrections improve testability; they do not constitute customer, integration or production evidence.

## Review limits and draft status

This is the author's adversarial review using public sources and earlier drafts, not an independent audit or feedback received from Spiral. Repository document commits and source checks are separate from product execution. No native product tests, live payments, pilot or deployment ran for this review, and no maintainer or Spiral feedback was solicited. Earlier versions remain historical records. The current English draft uses the edgepillar alias; public availability does not constitute submission.
