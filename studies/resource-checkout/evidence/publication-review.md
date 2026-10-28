# Publication review

Draft 0.3 | Review date: 28 October 2026 | Prepared by edgepillar

## Decision and scope

**GO for public availability as an independent, unsubmitted research draft.** Proceed only with bounded demand discovery. Implementation priority, funding readiness, real value operation and adoption claims remain unestablished. Public availability does not mean submission to Spiral or acceptance by its team.

This is an author's adversarial review of the repository from the perspective of a skeptical payments reviewer. It is not feedback received from Spiral, an independent security audit or qualification of any cited product. The review covers all current research documents, source claims, reachable repository history and the retained Word package.

## Corrections made

| Finding in the previous edition | Correction in Draft 0.3 |
| --- | --- |
| The experiment's fit with an adoption-scale question remained weak. | Add a reviewer brief, acknowledge the crypto-native niche and limit initial discovery to two weeks and three person-days. No implementation or funding priority is earned by technical possibility. |
| A service term could blur native cancellation eligibility and a longer provider promise. | Specify that the contract fixes an earliest cancellation height. It does not automatically expire the entry or accept a custom lease period. Separate any longer operator promise. |
| Order authorization and uncertain signing needed a more concrete contract. | Specify immutable order fields, integer denominations, invoice binding, durable job identity, account serialization, signer response loss and same-byte publication. Label all of this as proposed acceptance behavior. |
| Existing resource backend work was under-described. | Credit the shared executor, reservations, reconciliation, recycling and queue. Identify the stricter paid-order boundaries without claiming they already pass. |
| Similar native entries might be treated as interchangeable. | Require the original Fuse send hash and owner for delivery, not a beneficiary-and-amount match or aggregate plasma. Include paged and stale observations in the fault corpus. |
| A Lightning invoice could be counted as bitcoin spending without knowing the funding route. | Separate settled Lightning volume, self-reported BTC funding, fiat conversion, incentives and unknown funding. Unknowns do not satisfy the proposed BTC-spending continuation filter. |
| Distinct customers could overstate a pseudonymous sample. | Count eligible enrollment units, disclose Sybil and self-report limits, and avoid identity or wallet-balance collection. |
| Comparison and cost accounting needed tighter rules. | Prespecify assignment, missing outcomes and capacity interference. Separate free and paid denominators; assign routing costs to the actual payer and account for incoming liquidity, capital, support and remedies. |
| The Loupe description conflated a pitch with payment software. | Cite the landing-page design for a proposed go-zenon security scan. It establishes neither a wallet nor a completed scan or Spiral agreement. |
| The faucet description could imply free QSR provision. | Describe the cited HTLC token exchange accurately and exclude its activity from BTC demand. |
| Moving repository links and a short release revision were weak provenance. | Pin reviewed GitHub files to full commits and content hashes. Record the resolved release tag separately from binary provenance. Keep PR, release and external-page observations dated. |
| Fork default READMEs and separate active work were mixed. | Retain default-baseline limits and separately cite the open wallet contribution and desktop redesign drafts. Their reported CI and remaining acceptance gates are not requalified here. |
| The Word export could look like the latest proposal. | Retain Draft 0.2 for history and label it as superseded by Draft 0.3 Markdown. Earlier statements describe their dated revision, not the current product or publication state. |

## Source checks

The [source register](sources.json) records 62 public primary references. GitHub file observations include a full source commit, path, Git blob identity and SHA-256 of the reviewed file. PR and release observations include their reviewed state and available revision/date metadata. External documentation and forum pages include dated response hashes; those pages are not immutable.

The initial Loupe README lookup did not resolve because the repository has no README. Follow-up inspection identified and read its pinned design document; the corrected citation supports only the landing-page purpose. It does not convert the failed README lookup into a successful one.

Plasma Bot source, license and open contribution overlap were inspected. Its license is MIT in the reviewed snapshot, and no open issue or PR was listed at the observation time. This is a dated overlap check, not permission to change its code or a maintainer commitment. Inspect overlap again before implementation.

The review did not download release packages, reproduce cited CI, execute native software, verify activation or independently reproduce a developer-reported swap or benchmark. Existing failed or unexecuted qualification results remain separate from this document review. The current SPV limitations are kept explicit; no state-value or consensus-finality proof is assumed.

## Privacy and reachable history

The pre-edit repository had two reachable commits, two branch refs and twenty distinct file candidates. Every reachable blob was matched to the reviewed bytes. Both commit author and committer identities used the edgepillar alias and its GitHub noreply address. Current edited files receive the same review before publication; normal history is retained.

Checks covered visible text, filenames, links, JSON, commit messages and identities, and all XML and relationships inside the Word file. The retained package's core authors are edgepillar; its extra bibliography is empty and its thumbnail is blank. No macros, comments, embedded user objects, credentials, wallet material, real identity, private local paths or payment records were found in the reviewed material. Ordinary document and commit timestamps remain historical metadata. This is a scoped inspection, not an anonymity guarantee.

The inspected repository had no issues, pull requests, releases, workflow runs or Actions artifacts, with wiki and Pages disabled. Source captures, raw diagnostics, environment configuration and private storage records are excluded from the repository. Repository visibility and refs are checked again immediately before the publication action.

## What remains open

- Real demand at a concrete price after adequate free alternatives.
- Willing independent resource operators and a reviewed integration boundary.
- Actual adapter implementation, dependency and binary pins, active chain rules and durable signing/recovery acceptance.
- Operator inventory, payment-liability and compensation caps, plus independent acceptance before real value.
- A preregistered pilot that reports BTC funding uncertainty, task completion, costs and negative findings.

No product tests, live payments, pilot, deployment or message to Spiral was executed as part of this review. Document commits and source checks establish only the reviewed research artifact.
