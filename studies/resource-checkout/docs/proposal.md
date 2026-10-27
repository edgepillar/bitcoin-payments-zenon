# Bitcoin checkout for Zenon resource services

Draft 0.2 | Source observations through 28 October 2026 | Prepared by edgepillar

[Overview](../README.md) | [Proposal](proposal.md) | [Architecture](architecture.md) | [Experiment plan](experiment-plan.md) | [Sources](../evidence/sources.md)

The concrete delivery contract is in [Architecture](architecture.md). Comparators, metrics, proposed filters and failure qualification are in the [Experiment plan](experiment-plan.md). Recent ecosystem work is assessed in the [context appendix](ecosystem-context.md).

I propose a small test of BTC payments for an existing Zenon resource provisioner. A customer pays over Lightning; a provider allocates its own QSR to supply plasma to the customer's chosen Zenon address. The customer does not buy QSR for that service. The question is whether this creates useful, unsubsidized bitcoin spending that current free or native onboarding options do not already satisfy.

Zenon has no demonstrated advantage over Lightning for ordinary BTC payments in the evidence reviewed here. Its concrete addition is a native service that a Lightning payment can purchase. Lightning remains the payment rail. The proposed work is a checkout and delivery adapter plus a reusable recovery test suite, not another payment network or a new generic service marketplace.

Recommendation: proceed with demand discovery and a bounded integration design. Real value deployment and any claim of increased bitcoin adoption remain NO GO until customer demand, economics, delivery recovery and operator acceptance are established. This draft reports source review, not newly executed integration or live payment results.

## A specific service and its incremental value

Spiral's payments question requires evidence that people want to buy something with bitcoin. The relevant hypothesis here is narrow: someone who already needs a Zenon action may prefer paying sats for its resource provision instead of obtaining QSR or waiting for a constrained sponsor. The study must record that prior need; it must not manufacture a task solely to generate payments. [S01](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/README.md)

There is an existing implementation to build around. Plasma Bot exposes resource requests to people and software agents. Its roadmap plans native QSR or ZNN payments while retaining free flows. The proposed extension is a BTC option, subject to maintainer agreement and a fresh overlap check. No BTC integration or paid demand is established by those documents. [S04](https://github.com/0x3639/plasma.bot) [S05](https://github.com/0x3639/plasma.bot/blob/main/ROADMAP.md)

The underlying contract separates the QSR owner from its beneficiary. That lets a provider supply a chain specific resource while the customer keeps its QSR acquisition step out of the checkout. Other networks can also sell services for BTC; this is a concrete Zenon testbed, not an exclusive global capability. [S06](https://github.com/zenon-network/go-zenon/blob/v0.0.9-alphanet/vm/embedded/implementation/plasma.go) [S07](https://github.com/zenon-network/go-zenon/blob/dev/vm/embedded/definition/plasma.go)

| Need | Strong Lightning baseline | What Zenon adds here |
| --- | --- | --- |
| Paid APIs and sessions | L402, Aperture and existing wallet libraries already address this category. [S10](https://github.com/lightninglabs/L402/blob/master/protocol-specification.md) [S11](https://github.com/lightninglabs/aperture) | No unique payment capability is claimed. Reuse the existing gateway. |
| Conditional payment | LND supports hold invoice creation, settlement and cancellation. Application delivery and refunds still need terms. [S15](https://lightning.engineering/api-docs/api/lnd/invoices/add-hold-invoice/) [S16](https://lightning.engineering/api-docs/api/lnd/invoices/settle-invoice/) [S17](https://lightning.engineering/api-docs/api/lnd/invoices/cancel-invoice/) | A generic escrow is not sufficient justification for another chain. |
| Native resource allocation | Lightning checkout can pay a provider that calls the existing fusion API. | Zenon supplies the native resource; the adapter must demonstrate reliable delivery and demand. |
| Cross asset settlement | A different question from paying a provider who already owns inventory. | HTLC and PTLC work could support later research; neither is needed for this checkout. |
| Security and cost | BTC settlement and service completion remain separate. | No inherited bitcoin security, trustless BTC escrow, guaranteed throughput or zero total cost is claimed. |

A beneficiary address is required. The underlying action may still require a Zenon wallet and other assets. The proposal removes one resource acquisition step; it does not establish asset free access to every application. Existing proof of work and free sponsorship are mandatory alternatives in discovery. If they meet the same need adequately, a paid service may have no market.

## Evidence and the work that remains

The native service exists at source level; the paid integration is proposed. No new code, node, wallet, swap, benchmark or live chain qualification ran for this revision. Release evidence is separate from the binary, configuration and chain an operator actually uses. Preserve the original failed qualification results rather than treating a rewritten test or a green unrelated CI profile as acceptance.

| Dependency | Evidence and limit | Decision for the first experiment |
| --- | --- | --- |
| Resource backend | Existing Plasma Bot source and native fusion mechanism. The README and roadmap are not a paid SLA or a production audit. [S04](https://github.com/0x3639/plasma.bot) [S06](https://github.com/zenon-network/go-zenon/blob/v0.0.9-alphanet/vm/embedded/implementation/plasma.go) | Reuse candidate after source, license, interface and overlap review. No maintainer time is committed. |
| Lightning gateway | Existing L402 and Aperture work. The x402 Lightning specification is another target, not proof every SDK implements it. [S10](https://github.com/lightninglabs/L402/blob/master/protocol-specification.md) [S11](https://github.com/lightninglabs/aperture) [S12](https://github.com/x402-foundation/x402/blob/main/specs/schemes/exact/scheme_exact_lnbtc.md) | Qualify one adapter against immutable orders, durable claims and recovery first. |
| Core and SDK | v0.0.9 is released; active chain profile and SDK pairing still need capture. Dynamic Plasma identifiers are placeholders in the reviewed dev source. [S18](https://github.com/zenon-network/go-zenon/releases/tag/v0.0.9-alphanet) [S19](https://github.com/zenon-network/go-zenon/blob/dev/common/types/spork.go) [S37](https://github.com/digitalSloth/znn-typescript-sdk) | Use qualified existing rules. Do not make the first product depend on a future activation. |
| Native x402 PoC | Public recovery patterns are useful, but a pinned pending native trial failed an expectation and its correction was not executed. [S33](https://github.com/edgepillar/zenon-x402-poc) [S34](https://github.com/edgepillar/zenon-x402-poc/blob/6a0af7d6c96fe770b7c141c44894536f2a543b68/docs/P1_NATIVE_V4_PENDING_LOCAL_QUALIFICATION.md) | Review patterns as research. Its native settlement path is not a prerequisite for Lightning paid fusion. |
| Proof and contracts | StateRoot candidates, PTLC and ZVM address other problems and have separate acceptance boundaries. [S31](https://github.com/digitalSloth/go-zenon/blob/feature/merkle-state-root/chain/nom/momentum.go) [S24](https://github.com/zenon-network/go-zenon/pull/138) [S39](https://github.com/Zenoglyphs-VM/zvm-docs/blob/main/ARCHITECTURE.md) | Keep them off the initial critical path; do not advertise guarantees they have not established. |

Before implementation, identify the target maintainer or operator, inspect current issues and open changes, pin the source and dependencies, and agree the permitted adapter boundary. Before any real value test, an independent reviewer and operator must accept the actual software, inventory exposure, recovery and compensation policy. This proposal neither requests nor assumes that approval now.

## Deliverables and a proportionate request to Spiral

The first deliverable is the discovery record and a go or stop decision. If demand survives, the next deliverable is one adapter with an order schema, protected inventory policy, durable recovery, conformance tests, fault fixtures and a sanitized measurement schema. Reuse existing projects and libraries. A source and security review should size the implementation before hours or funding are committed.

I would ask Spiral for critique of the payments hypothesis and outcome definitions, and, if the use case is useful, introductions to a Lightning integration reviewer or measurement collaborator. No token endorsement, partnership, grant, operator role or maintainer commitment is implied. The first discussion should be a focused experiment proposal; it has not earned a claim to be a solution to bitcoin adoption. [S02](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/CONTRIBUTING.md) [S03](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/.github/ISSUE_TEMPLATE/moonshot-idea.yml)

Regardless of the commercial result, the useful public output would be a source pinned account of paid service recovery, delivery failures, costs and customer choices. Publish negative findings as well as successful payments. Keep real identity, raw user records, private paths and account linkage out of the release. This remains an unsubmitted draft by edgepillar.
