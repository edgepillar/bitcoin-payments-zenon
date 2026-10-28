# Bitcoin checkout for Zenon resource services

**Draft research proposal. No production implementation, executed pilot or adoption result is claimed.**

This study asks whether a customer who already needs Zenon resources would pay BTC over Lightning for a provider to supply plasma to a chosen beneficiary address. The provider uses its own QSR inventory. The customer need not acquire QSR for that resource service, although the underlying task may still require a Zenon wallet and other assets.

Zenon's concrete role is the native resource service. Lightning remains the payment rail. The reviewed evidence does not demonstrate a general Zenon advantage over Lightning for ordinary BTC payments. Existing free provision and proof of work are part of the comparison; they may eliminate the commercial case.

The proposed starting point is an optional BTC checkout around an existing resource provider. Plasma Bot already documents a service and agent API, and its roadmap plans QSR or ZNN payments while retaining free flows. BTC support and paid demand are not established by those documents. [Existing service](https://github.com/0x3639/plasma.bot/blob/ada5a03a458c17c18083fcc099276248e8f611fe/README.md), [roadmap](https://github.com/0x3639/plasma.bot/blob/ada5a03a458c17c18083fcc099276248e8f611fe/ROADMAP.md).

## Read the study

| Document | What it contains |
| --- | --- |
| [Reviewer brief](docs/reviewer-brief.md) | The current decision, fit with Spiral's goal and the strongest objections |
| [Proposal](docs/proposal.md) | Customer need, the incremental service, Lightning baselines, evidence limits and deliverables |
| [Architecture](docs/architecture.md) | Immutable orders, inventory, signer boundaries, delivery observations and recovery |
| [Experiment plan](docs/experiment-plan.md) | Adequate free alternatives, intended task completion, BTC uptake, economics and stop conditions |
| [Critical review](docs/critical-review.md) | Ten objections to the earlier draft and the changes made in response |
| [Ecosystem context](docs/ecosystem-context.md) | The relevance and limits of recent Zenon developments across the ecosystem |
| [Possible submission](docs/submission-draft.md) | An unsubmitted short discussion draft |
| [Sources](evidence/sources.md) | The 62 public primary references and their scope; [JSON](evidence/sources.json) is canonical for the source index |
| [Claim ledger](evidence/claims.md) | Source observations, proposed design and claims that remain unestablished |
| [Publication review](evidence/publication-review.md) | Source checks, corrected claims, privacy scope and remaining gates |
| [Historical Word export](exports/README.md) | Draft 0.2 retained for history; Draft 0.3 Markdown supersedes it |

## Current decision

Proceed with demand discovery capped at two weeks and three person-days. Any implementation must first resolve demand, source overlap and the proposed operator boundary. This is a small crypto-native testbed, not a demonstrated adoption moonshot or a funding-ready integration. Real value operation, production readiness and increased adoption claims require separate acceptance evidence.

The proposed experiment distinguishes three questions:

1. Does offering BTC payment help people complete an already intended task when existing alternatives remain available?
2. Does a durable fulfillment worker improve delivery compared with assisted manual fulfillment using the same Lightning rail and service terms?
3. Will customers pay enough to cover routing, compensation, QSR capital, infrastructure and support?

A payment method shift alone does not establish additional economic activity. A small sample of people who already need a crypto native service does not establish mainstream merchant adoption. Proposed sample sizes and continuation filters are planning choices, not measured results or statistical significance thresholds.

A settled Lightning invoice also does not establish that a customer spent a held BTC balance. Report self-reported BTC funding, fiat-funded routing, incentives and unknown funding separately. Privacy-preserving enrollment pseudonyms are not proof of distinct humans.

## Evidence status

Source observations are dated through 28 October 2026. A source file, merged change, release, developer report and actual deployed behavior are different evidence levels. Draft 0.3 records reviewed GitHub file commits, content hashes and dated PR/release observations. External pages and repository metadata retain explicit limits. This source register is not an execution manifest.

This repository contains research documents and a prior document export. It does not contain a payment adapter implementation. No native runtime tests, hosted product tests, live payments, activation checks or pilot were executed as part of this repository preparation. Document integrity and privacy checks do not qualify the proposed system.

## Independence and draft status

Prepared by **edgepillar** for possible discussion of the questions raised in Spiral's [bitcoin payments report](https://github.com/spiralxyz/bitcoin-payments). This is independent research, not a statement on behalf of Spiral, Zenon maintainers, Plasma Bot or any other project. No submission, partnership, endorsement, funding or maintainer commitment is implied.

See [CHANGELOG](CHANGELOG.md), [contribution guidance](CONTRIBUTING.md) and [NOTICE](NOTICE.md).
