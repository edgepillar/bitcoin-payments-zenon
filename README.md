# Bitcoin payments and Zenon: research draft

**Independent research by edgepillar. Draft 0.3. Not submitted to Spiral.**

Start with the [reviewer brief](studies/resource-checkout/docs/reviewer-brief.md) and [full proposal](studies/resource-checkout/docs/proposal.md).

The proposal tests a BTC checkout for an existing Zenon resource service. Lightning carries the payment; the provider fuses its own QSR for the customer's chosen beneficiary. The possible benefit is removing a QSR acquisition step for someone who already needs that service. Free sponsorship and proof of work may eliminate the paid market.

There is no demonstrated general Zenon advantage over Lightning for ordinary BTC payments, no measured demand and no established route to broad adoption. The current recommendation is bounded discovery, not an implementation or funding commitment. Generic Lightning fulfillment and recovery findings could be useful even if this particular paid service fails.

| Read | Purpose |
| --- | --- |
| [Reviewer brief](studies/resource-checkout/docs/reviewer-brief.md) | Fit with Spiral's question, strongest objections and current decision |
| [Proposal](studies/resource-checkout/docs/proposal.md) | Customer need, alternatives and a proportionate request for critique |
| [Architecture](studies/resource-checkout/docs/architecture.md) | Exact delivery object, order binding, inventory, signer and recovery contract |
| [Experiment plan](studies/resource-checkout/docs/experiment-plan.md) | BTC funding, task completion, economics, privacy and stop conditions |
| [Critical review](studies/resource-checkout/docs/critical-review.md) | Corrections to earlier claims and remaining objections |
| [Ecosystem context](studies/resource-checkout/docs/ecosystem-context.md) | Relevant developments with source, release and activation kept distinct |
| [Sources](studies/resource-checkout/evidence/sources.md) | Public primary references and exact source scope; [JSON](studies/resource-checkout/evidence/sources.json) |
| [Publication review](studies/resource-checkout/evidence/publication-review.md) | Source checks, corrections, privacy scope and evidence limits |
| [Historical Word export](studies/resource-checkout/exports/README.md) | Draft 0.2 retained for history; superseded by Draft 0.3 Markdown |

This repository contains documents. It has no implemented payment adapter, executed pilot, product benchmark or independent security certification. Publication does not mean submission, endorsement, funding, partnership or an operator commitment. No messages to Spiral accompany this repository.

Original research documentation retains the [CC BY 4.0 license](LICENSE). Cited third party material retains its own terms. See the study's [contribution guidance](studies/resource-checkout/CONTRIBUTING.md), [notice](studies/resource-checkout/NOTICE.md) and [revision history](studies/resource-checkout/CHANGELOG.md).
