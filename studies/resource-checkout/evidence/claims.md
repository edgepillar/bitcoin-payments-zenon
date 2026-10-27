# Claim ledger

Draft 0.2. These classifications describe the research evidence. They do not establish deployed behavior.

| ID | Statement | Classification | Evidence or next boundary |
| --- | --- | --- | --- |
| C01 | A provider can own QSR while a selected beneficiary receives the resource benefit. | Source observation | [S06](https://github.com/zenon-network/go-zenon/blob/v0.0.9-alphanet/vm/embedded/implementation/plasma.go); actual operator rules must be qualified. |
| C02 | Existing Lightning tools are a strong baseline for paid APIs and conditional invoices. | Source observation | [S10](https://github.com/lightninglabs/L402/blob/master/protocol-specification.md) [S11](https://github.com/lightninglabs/aperture) [S15](https://lightning.engineering/api-docs/api/lnd/invoices/add-hold-invoice/) [S16](https://lightning.engineering/api-docs/api/lnd/invoices/settle-invoice/) [S17](https://lightning.engineering/api-docs/api/lnd/invoices/cancel-invoice/); qualify the chosen implementation. |
| C03 | A BTC checkout might remove one QSR acquisition step for a customer who already needs the service. | Proposed integration hypothesis | Test against adequate free and native alternatives; willingness to pay is unknown. |
| C04 | Plasma Bot already documents a provisioner and agent API; its roadmap proposes native payments. | Source and roadmap observations | [S04](https://github.com/0x3639/plasma.bot) [S05](https://github.com/0x3639/plasma.bot/blob/main/ROADMAP.md); BTC support and a paid SLA are not established here. |
| C05 | The current SPV verification contract does not authenticate state values or establish consensus finality. | Bounded source contract | [S29](https://github.com/edgepillar/zenon-spv/blob/main/docs/verification-contract.md); delivery observations retain explicit operator trust. |
| C06 | The cited native x402 pending trial failed an expectation; its documented correction was unexecuted. | Pinned reported result | [S34](https://github.com/edgepillar/zenon-x402-poc/blob/6a0af7d6c96fe770b7c141c44894536f2a543b68/docs/P1_NATIVE_V4_PENDING_LOCAL_QUALIFICATION.md); do not infer that every current branch or other test has the same outcome. |
| C07 | The proposed checkout is an atomic BTC to resource exchange or a trustless BTC escrow. | Not established and not claimed | Upfront payment leaves provider delivery and compensation obligations. |
| C08 | Dynamic Plasma or another upgrade is active on the selected live chain. | Not established by this preparation | [S19](https://github.com/zenon-network/go-zenon/blob/dev/common/types/spork.go); binary, chain and enforcement evidence are separate acceptance inputs. |
| C09 | The proposed numeric sample sizes and commercial filters are measured outcomes. | False interpretation | They are planning choices in the [experiment plan](../docs/experiment-plan.md). |
| C10 | Offering BTC checkout increases total task completion or broad bitcoin adoption. | Not established | Record task completion and payment share separately; a small crypto native sample cannot establish mainstream adoption. |
| C11 | The proposed adapter is implemented, independently accepted or ready for real value. | Not established | There is no implementation in this repository; demand, engineering and operator gates remain open. |

No new native runtime, live chain, wallet, swap or product benchmark evidence was created by preparing these documents. Failed or unknown prior results are not overwritten by document revisions.
