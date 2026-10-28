# Reviewer brief

Draft 0.3 | 28 October 2026 | Independent research by edgepillar | Not submitted to Spiral

**Decision:** suitable for public discussion as a falsifiable research draft. Proceed with bounded demand discovery only. Do not present this as a demonstrated solution to bitcoin adoption, a funding-ready integration or an accepted live payment system.

## Why this might matter

Test whether a person with an existing Zenon resource need and BTC to spend would pay a resource provider over Lightning instead of acquiring QSR. The provider owns and fuses the QSR; the customer keeps their keys. Existing free sponsorship and proof of work may already solve the problem adequately. The discovery study should be allowed to reject the paid product.

Lightning supplies the payment capability. Zenon supplies the native service being purchased. The service is specific to Zenon, but the generic paid API and recovery design is not a unique Zenon property. No extra BTC bridge, token representation, generic escrow or consensus upgrade is justified for this experiment. [Proposal](proposal.md)

## The strongest objections

| Reviewer objection | Response and remaining gate |
| --- | --- |
| This is a small crypto-native niche, while Spiral asks for adoption at scale. | Correct. There is no established market size or distribution advantage. Limit discovery to two weeks and three person-days; do not prioritize an implementation or funding request without evidence. |
| People can obtain the resource free. | Keep adequate free routes available and record their availability and delay. Stop if they satisfy the need. |
| A Lightning invoice does not prove a customer spent bitcoin they held. | Separate settled Lightning volume, self-reported BTC-funded spending, fiat-funded use, incentives and unknown funding. Do not classify unknowns as bitcoin spenders. |
| A fusion is not a guaranteed number of transactions or a custom lease. | Sell an identified allocation under qualified native rules. Cancellation eligibility is a height condition, not automatic expiry or a stronger provider promise. |
| Successful payment does not prove delivery. | Bind an immutable order to one native job and inspect the exact owner-indexed fusion entry and contract outcome. Keep unknown outcomes and remedies visible. |
| Existing Plasma Bot code is enough. | It is a reuse candidate, not an assumed paid service backend. Its public API and FIFO recycling policy need explicit adaptation before a paid service promise. |
| The useful parts could be implemented without Zenon. | Use a generic paid-service control and publish the reusable Lightning failure cases separately from native resource delivery. |

## What a successful next step would produce

First produce a short discovery record describing prior customer tasks, adequate alternatives, offered prices, provider costs and a go or stop decision. The interview and continuation counts are planning filters, not market evidence. No team, operator, funding or review commitment is assumed.

If that gate passes, agree a source-pinned adapter boundary with a willing resource operator, qualify the order and recovery contract, and obtain independent acceptance before any real value. Only then consider the bounded feasibility pilot. Its outcomes separate task completion, BTC funding, payment method choice, automation, costs and unresolved liabilities. [Architecture](architecture.md), [experiment plan](experiment-plan.md)

The proposal does not solve acquiring bitcoin, volatility, tax friction, merchant distribution or the preference to hold BTC. Any broader adoption argument must come from later evidence rather than the existence of a technically possible checkout.

## Reading and evidence

Read the [proposal](proposal.md), [source register](../evidence/sources.md), [claim ledger](../evidence/claims.md) and [publication review](../evidence/publication-review.md). Recent ecosystem work is retained in the [context appendix](ecosystem-context.md), with source, release, reported operation and activation kept distinct.

The repository contains documents, not an adapter implementation, executed pilot or independent security certification. The Word file is a historical Draft 0.2 export; Draft 0.3 Markdown supersedes it. No contact with Spiral is implied by public availability.
