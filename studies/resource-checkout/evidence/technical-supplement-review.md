# Technical supplement review

Draft 0.4 | 28 October 2026 | Prepared by edgepillar

This edition selectively adds independently written technical synthesis from reviewed public sources. It preserves the Draft 0.3 core proposal, discovery-first decision and historical Word export. It does not import an external report verbatim or assert rights over its text, missing companion inventory or private evidence.

## Disposition of the additional research material

| Topic | Disposition and reason |
| --- | --- |
| PTLC reclaim-lock extension | Adopt as an optional, source-pinned research update. Its terms/key and upgrade-compatibility distinctions belong in future conversion qualification. |
| HTLC/PTLC/Lightning and LP exposure | Clarify the separate mechanisms and trust roles. None becomes a prerequisite for the first BTC-paid fusion service. |
| RPC and pending-state changes | Add source/capability context and proposed failure cases. Do not turn development merges into binary or deployment acceptance. |
| Decoder/snapshot warning | Retain the reported baseline and conditional reachability. Reject a universal zero-remote-crash interpretation. |
| Native HTTP-resource binding and signer APIs | Adapt as compatibility requirements. Interactive sign-and-publish is distinct from detached signing; an open SDK issue alone proves neither delivery nor absence. |
| Changed quote/resource replay | Add an explicit proposed case: one immutable payment cannot create another independent entitlement by changing order metadata. Preserve legitimate L402 reuse and scheme-specific replay behavior. |
| Broad multi-rail gateway, swaps, credits and ZVM | Defer to separately justified research. These do not establish a customer need or improve the initial dependency case. |
| Invoice equals BTC spending | Reject. Keep held-BTC, fiat conversion, incentive and unknown categories with the existing self-report and denominator limits. |
| Public raw journals and counterparty linkage | Reject as a default publication policy. Keep necessary protected evidence separate from sanitized aggregates and agreed role aliases. |

## What changed

- Add [optional interoperability boundaries](../docs/interop-research-boundaries.md), including eight unexecuted future fault vectors.
- Add a [protocol, signer and node matrix](../docs/compatibility-matrix.md).
- Extend the ecosystem context and the proposed experiment fault matrix.
- Append source IDs S63-S73 while preserving the earlier S01-S62 records and their dated meaning.
- Preserve the central [proposal](../docs/proposal.md), funding methodology, original native-hash delivery identity and historical export.

The new pinned PTLC files were read at PR #216's merge revision. Other selected source files are reused from the completed dated source review; their recorded observation dates are retained rather than relabeled as fresh executions. PR and issue metadata are observations, not immutable runtime evidence. The [source register](sources.json) records exact file paths, commits and content hashes where applicable.

## Validation and limits

Publication checks cover candidate bytes, relative links, source IDs, manifest hashes, English text, privacy patterns and commit identity. No code, crypto execution, native test, CI rerun, chain query, deployment, signature, swap or payment is performed for this supplement. New fault cases are specifications, not test results.

Source inspection does not qualify an installed binary, live spork state, signer, recipient receive, native state proof or consensus finality. Existing failed or unexecuted qualification records retain their original scope. An operator, inventory/compensation policy and independent acceptance remain necessary before real value.

Public availability does not submit the work to Spiral or commit any maintainer's time. Raw source captures, private diagnostics, local paths, wallet material and payment-to-address linkage are excluded.
