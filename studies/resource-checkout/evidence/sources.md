# Source register

Draft source observations through 28 October 2026. The [JSON index](sources.json) records reference types and unresolved pins. A moving branch or repository link is not an immutable execution input. Scope notes limit what each source can support.

| ID | Public primary source | Reference type | Scope |
| --- | --- | --- | --- |
| S01 | [Spiral report on bitcoin payments](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/README.md) | commit in citation | Pinned report; motivation and scope, not evidence that this experiment will succeed. |
| S02 | [Spiral contribution guidance and moonshot template](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/CONTRIBUTING.md) | commit in citation | Pinned contribution guidance. The companion short draft follows the moonshot fields. |
| S03 | [Spiral moonshot issue fields](https://github.com/spiralxyz/bitcoin-payments/blob/5320295278e7ce3b5e1cb2d196def7a0fde3d729/.github/ISSUE_TEMPLATE/moonshot-idea.yml) | commit in citation | Pinned template used to structure the companion submission draft. |
| S04 | [Plasma Bot implementation overview](https://github.com/0x3639/plasma.bot) | repository | Existing provisioner and agent API; source documentation, not a deployment or commercial demand audit. |
| S05 | [Plasma Bot roadmap](https://github.com/0x3639/plasma.bot/blob/main/ROADMAP.md) | mutable ref in citation | Current agent API; planned QSR or ZNN payments and MCP integration. BTC support is proposed here, not established. |
| S06 | [Fusion and cancellation implementation](https://github.com/zenon-network/go-zenon/blob/v0.0.9-alphanet/vm/embedded/implementation/plasma.go) | tag in citation | Release tag source. Owner, beneficiary and cancellation behavior; exact deployed rules remain an acceptance gate. |
| S07 | [Fusion entry definition](https://github.com/zenon-network/go-zenon/blob/dev/vm/embedded/definition/plasma.go) | mutable ref in citation | Dated dev source for entry identity and beneficiary fields; not a deployed chain profile. |
| S08 | [Fusion and plasma RPC at the release tag](https://github.com/zenon-network/go-zenon/blob/v0.0.9-alphanet/rpc/api/embedded/plasma.go) | tag in citation | Entries are listed by owner. Beneficiary plasma is an aggregate, not an order receipt. |
| S09 | [Fusion constants at the release tag](https://github.com/zenon-network/go-zenon/blob/v0.0.9-alphanet/vm/constants/embedded.go) | tag in citation | Contains environment dependent values; do not infer a universal lease duration from this file alone. |
| S10 | [L402 protocol specification](https://github.com/lightninglabs/L402/blob/master/protocol-specification.md) | mutable ref in citation | Existing protocol; a separate adapter and compatibility target. |
| S11 | [Aperture paid API proxy](https://github.com/lightninglabs/aperture) | repository | Existing service gateway and session or metered payment work; prior art for the baseline. |
| S12 | [x402 exact lnbtc specification](https://github.com/x402-foundation/x402/blob/main/specs/schemes/exact/scheme_exact_lnbtc.md) | mutable ref in citation | Specification in main as reviewed on 28 October 2026; implementation coverage must be tested. |
| S13 | [LDK Node](https://github.com/lightningdevkit/ldk-node) | repository | Existing Lightning integration building block; deployment suitability remains an operator decision. |
| S14 | [Bitcoin Development Kit](https://github.com/bitcoindevkit/bdk) | repository | Existing bitcoin wallet building block; no new wallet cryptography is proposed. |
| S15 | [LND AddHoldInvoice](https://lightning.engineering/api-docs/api/lnd/invoices/add-hold-invoice/) | documentation url | Existing conditional payment primitive; not a quality oracle or proof of cross chain atomicity. |
| S16 | [LND SettleInvoice](https://lightning.engineering/api-docs/api/lnd/invoices/settle-invoice/) | documentation url | Settles an accepted invoice. Its semantics differ from x402 proof consumption. |
| S17 | [LND CancelInvoice](https://lightning.engineering/api-docs/api/lnd/invoices/cancel-invoice/) | documentation url | Canceling a settled invoice fails; cancellation is not a refund of a completed payment. |
| S18 | [go zenon v0.0.9 alphanet release](https://github.com/zenon-network/go-zenon/releases/tag/v0.0.9-alphanet) | release tag | Release dated 10 October 2026 at bb39e31; release existence does not prove activation. |
| S19 | [Current dev spork definitions](https://github.com/zenon-network/go-zenon/blob/dev/common/types/spork.go) | mutable ref in citation | Reviewed on 28 October 2026. Dynamic Plasma and libp2p identifiers are placeholders in this source. |
| S20 | [Dynamic Plasma PR 63](https://github.com/zenon-network/go-zenon/pull/63) | pull request | Merged to dev; candidate resource pricing work, not an observed mainnet activation. |
| S21 | [Community spork renewal PR 101](https://github.com/zenon-network/go-zenon/pull/101) | pull request | Merged protocol change; operators and actual chain enforcement remain separate checks. |
| S22 | [Receive recipient integrity PR 182](https://github.com/zenon-network/go-zenon/pull/182) | pull request | Merged 22 October 2026; scope differs between non mainnet rules and historical mainnet behavior. |
| S23 | [Pillar Update repricing PR 183](https://github.com/zenon-network/go-zenon/pull/183) | pull request | Merged 20 October 2026; its replacement policy must not be copied into customer payment recovery. |
| S24 | [PTLC contract PR 138](https://github.com/zenon-network/go-zenon/pull/138) | pull request | Merged 15 October 2026 into dev. Contract activation and client swap safety are separate. |
| S25 | [Ferry implementation and security model](https://github.com/sol-znn/ferry-web/blob/master/docs/SECURITY.md) | mutable ref in citation | Existing HTLC client and explicit browser, deployment and recovery limitations. |
| S26 | [Ferry developer report](https://forum.zenon.org/t/ferry-multi-chain-htlc-web-service/2366) | documentation url | Developer reports a mainnet BTC and ZNN swap. This proposal did not independently reproduce it. |
| S27 | [PTLC console](https://github.com/sol-znn/ptlc-console) | repository | Demonstration tooling; simulated bitcoin transactions in the console are distinct from regtest blocks. |
| S28 | [PTLC research](https://github.com/edgepillar/ptlc-research) | repository | Public research and recovery work; independent acceptance remains a separate gate. |
| S29 | [Zenon SPV verification contract](https://github.com/edgepillar/zenon-spv/blob/main/docs/verification-contract.md) | mutable ref in citation | Bounded v1 and v2 verification and explicit trust assumptions; state values remain unsupported. |
| S30 | [State commitment audit](https://github.com/edgepillar/zenon-spv/blob/main/docs/state-commitment-audit.md) | mutable ref in citation | Audit baseline and commitment distinctions; it is not a statement about every later fork. |
| S31 | [Candidate state root header](https://github.com/digitalSloth/go-zenon/blob/feature/merkle-state-root/chain/nom/momentum.go) | mutable ref in citation | Candidate branch containing a v3 header commitment; no acceptance or activation claim. |
| S32 | [Candidate state tree preparation](https://github.com/digitalSloth/go-zenon/blob/feature/merkle-state-root/docs/STATE_TREE_PREBUILD.md) | mutable ref in citation | Operator preparation for the candidate; provenance and verifier compatibility still need qualification. |
| S33 | [Zenon x402 proof of concept](https://github.com/edgepillar/zenon-x402-poc) | repository | Research adapter and recovery work; not an official x402 network or production deployment. |
| S34 | [Pinned x402 native pending qualification outcome](https://github.com/edgepillar/zenon-x402-poc/blob/6a0af7d6c96fe770b7c141c44894536f2a543b68/docs/P1_NATIVE_V4_PENDING_LOCAL_QUALIFICATION.md) | commit in citation | Immutable source revision: V4 pending trial failed an expectation; V5 correction was not executed. |
| S35 | [Syrius Extension v0.3.7](https://github.com/sol-znn/syrius-extension/releases/tag/v0.3.7) | release tag | Release dated 22 October 2026 at bec8791; later branch work is a different artifact. |
| S36 | [Syrius Extension integration contract](https://github.com/sol-znn/syrius-extension/blob/master/docs/INTEGRATION.md) | mutable ref in citation | Origin permission and signing boundary; browser and mobile paths require distinct tests. |
| S37 | [Zenon TypeScript SDK](https://github.com/digitalSloth/znn-typescript-sdk) | repository | Client implementation; versions and active node semantics must be matched. |
| S38 | [Zenon SDK specification](https://github.com/0x3639/zenon-sdk-spec) | repository | Language neutral specification and vectors; not proof that a new network profile is deployed. |
| S39 | [ZVM architecture](https://github.com/Zenoglyphs-VM/zvm-docs/blob/main/ARCHITECTURE.md) | mutable ref in citation | Eighteen repository devnet architecture based on NoM ordering and EVM derivation. |
| S40 | [ZVM committee operations](https://github.com/Zenoglyphs-VM/zvm-docs/blob/main/operations/COMMITTEE.md) | mutable ref in citation | Threshold vault operations; collusion and availability remain material trust assumptions. |
| S41 | [ZVM future development](https://github.com/Zenoglyphs-VM/zvm-docs/blob/main/planning/FUTURE.md) | mutable ref in citation | Separates proposed additions such as trustless peg out from implemented behavior. |
| S42 | [ZVM fleet benchmark results](https://github.com/Zenoglyphs-VM/zvm-docs/blob/main/benchmarks/results/FLEET-v2.md) | mutable ref in citation | Developer reported devnet measurements; not mainnet capacity or an independent benchmark. |
| S43 | [Mutable multisig PR 72](https://github.com/zenon-network/go-zenon/pull/72) | pull request | Draft protocol work as reviewed; not an active wallet capability. |
| S44 | [Governance ZIP working draft](https://forum.hypercore.one/t/draft-governance-zip-working-draft-for-comment/935) | documentation url | Draft governance work; distinct from the merged community spork renewal. |
| S45 | [nomctl operator tooling](https://github.com/0x3639/nomctl) | repository | Operational tooling; node or bridge health must still be measured in the chosen environment. |
| S46 | [Existing bridge frontend](https://github.com/sol-znn/bridge.mainnet.zenon.community) | repository | Existing bridge application; repository changes do not establish live bridge availability. |
| S47 | [Bridge orchestrator development](https://github.com/0x3639/orchestrator) | repository | Bridge service development; no production health or custody guarantee is inferred. |
| S48 | [Loupe](https://github.com/zenon-network/loupe) | repository | Wallet and payments coordination work; no partnership, deployment or user demand is assumed. |
| S49 | [Zenon Portal research](https://github.com/TminusZ/zenon-developer-commons/blob/main/docs/specs/Zenon%20Portal/Portal%20V2/zenon_portal_final.md) | mutable ref in citation | Research design; the document name does not establish an implementation or independent audit. |
| S50 | [Zenon core specification](https://github.com/0x3639/go-zenon-spec) | repository | Reference work with an older pinned baseline; not current core conformance certification. |
| S51 | [nom webwallet](https://github.com/digitalSloth/nom-webwallet) | repository | Additional wallet surface; release, custody and integration evidence must be checked separately. |
| S52 | [Official Syrius wallet](https://github.com/zenon-network/syrius) | repository | Separate wallet implementation and release lineage; do not combine fork evidence. |
| S53 | [Syrius community fork](https://github.com/maznnwell/syrius) | repository | Community wallet work; branch and release evidence remain specific to this repository. |
| S54 | [Syrius redesign work](https://github.com/sol-znn/syrius) | repository | Separate redesign work; a specification or branch is not a shipped release. |
| S55 | [Zenon faucet](https://github.com/sol-znn/zenon-faucet) | repository | Test onboarding application; not a treasury custody model. |
| S56 | [ZTS airdrop tooling](https://github.com/sol-znn/zts-airdrop) | repository | Distribution tooling; airdrop activity does not establish paid bitcoin demand. |
