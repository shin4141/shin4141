# Shin

Independent researcher and builder working on AI systems, boundary integrity, and Decision-OS.

**24 direct upstream merges across 20 independent public repositories.**

These are public OSS contributions, not client engagements or evidence of paid commercial conversion.

I focus on consequential state transitions — places where a system says something is complete, settled, authorized, recorded, cancelled, or recovered, but the underlying state does not fully support that claim.

**I don’t just fix the broken point. I repair the transition so the system can move forward without carrying the same failure into its next state.**

Typical boundaries: retry, rollback, replay, partial progress, authority changes, durable state, payment / settlement state, and AI-agent handoff.

## Public upstream acceptance — technical repair evidence

Each link exposes the failure boundary, bounded repair, and third-party upstream acceptance:

- **[Apple / swift-openapi-generator #939](https://github.com/apple/swift-openapi-generator/pull/939) — developer tooling / deterministic failure handling.** Distinct OpenAPI components could collapse to the same generated Swift type name and crash recursive-type boxing → detect collisions before boxing, emit a deterministic diagnostic, and cover the regression → maintainer feedback was addressed, then the patch was approved and merged.
- **[Sony / nmos-cpp #520](https://github.com/sony/nmos-cpp/pull/520) — protocol / validation boundary.** Non-six-octet interface IDs could make IS-04 Node resources schema-invalid → apply repository-native regex validation, the existing schema-valid fallback, and expanded malformed-input tests → maintainer-requested changes were incorporated and the patch was merged.
- **[Vercel / workflow #3575](https://github.com/vercel/workflow/pull/3575) — atomic state / recovery.** A step row could commit without its replay event and wedge later replay → write both in one transaction while preserving recovery for existing orphan rows → the upstream reviewer approved and merged the patch.
- **[Adyen / adyen-node-api-library #1760](https://github.com/Adyen/adyen-node-api-library/pull/1760) — payment infrastructure / public API contract.** The public Session Authentication API lacked its generated models in the public `Types` namespace → add the missing export and test it through the package entrypoint → a human reviewer thanked, approved, and merged the patch.
- **[Dynawo / DyCoV #385](https://github.com/dynawo/dyn-grid-compliance-verification/pull/385) — power-grid compliance tooling / explicit correctness acceptance.** A missing parameter set produced an empty XPath result that bypassed absence handling → treat the empty result as missing and add regression coverage → the maintainer stated “the change is correct,” extended Shin’s branch with the adjacent fix and tests, verified 778 passed and `ruff` clean, and merged.

### Merge portfolio

All 24 verified merges are linked in this README: the two 2026-08-24 additions are featured above; the 22 earlier merges remain grouped below by boundary type.

![STATE / TRANSITION ×6](https://img.shields.io/badge/STATE%20%2F%20TRANSITION-6-1f6feb?style=flat-square&labelColor=1f6feb) ![DATA / CONTEXT ×4](https://img.shields.io/badge/DATA%20%2F%20CONTEXT-4-8250df?style=flat-square&labelColor=8250df) ![CONFIG / POLICY ×4](https://img.shields.io/badge/CONFIG%20%2F%20POLICY-4-9a6700?style=flat-square&labelColor=9a6700) ![RETRY / RECOVERY ×2](https://img.shields.io/badge/RETRY%20%2F%20RECOVERY-2-1a7f37?style=flat-square&labelColor=1a7f37) ![INSTALL / COMPLETION ×2](https://img.shields.io/badge/INSTALL%20%2F%20COMPLETION-2-bc4c00?style=flat-square&labelColor=bc4c00) ![TRANSPORT / PARTIAL PROGRESS ×1](https://img.shields.io/badge/TRANSPORT%20%2F%20PARTIAL%20PROGRESS-1-0e7490?style=flat-square&labelColor=0e7490) ![NUMERIC / REPRESENTATION ×3](https://img.shields.io/badge/NUMERIC%20%2F%20REPRESENTATION-3-cf222e?style=flat-square&labelColor=cf222e)

![STATE / TRANSITION ×6](https://img.shields.io/badge/STATE%20%2F%20TRANSITION-6-1f6feb?style=flat-square&labelColor=1f6feb)

- [Questboard #151](https://github.com/rictaworks/questboard/pull/151) — existing-member invite state and truthful role visibility → **MERGED**
- [Weftmap #175](https://github.com/DataDave-Dev/weftmap/pull/175) — stale graph and error invalidation across workspace context changes → **MERGED**
- [makoto2 #56](https://github.com/pooza/makoto2/pull/56) — process-state truth / permission handling; maintainer reproduced the failure and re-verified the repair with real `EACCES` → **MERGED**
- [Codesema #32](https://github.com/getCodesema/codesema-cli/pull/32) — renamed and copied preview entries retain the destination path used for later status and diff lookup → **MERGED**
- [Mercur #1399](https://github.com/mercurjs/mercur/pull/1399) — terminal payment evidence is counted once so fully captured/refunded collections do not collapse into false partial states → **MERGED**
- [Vercel Workflow #3575](https://github.com/vercel/workflow/pull/3575) — the step entity and matching `step_created` event now commit atomically, while old partial-write orphans can still be drained without losing replay history → **MERGED**

![DATA / CONTEXT ×4](https://img.shields.io/badge/DATA%20%2F%20CONTEXT-4-8250df?style=flat-square&labelColor=8250df)

- [PyScrappy #148](https://github.com/mldsveda/PyScrappy/pull/148) — derived-selector context inheritance; maintainer independently verified the repair locally and confirmed the regression coverage → **MERGED**
- [Job Autofill #215](https://github.com/ritsth/job-autofill-extension/pull/215) — preserve known metadata when blank inputs would otherwise overwrite it → **MERGED**
- [Job Autofill #221](https://github.com/ritsth/job-autofill-extension/pull/221) — company detection falls back to trimmed image alt text when visible text is absent; visible text retains priority; blank alt values preserve selector fallthrough → **MERGED**
- [RDKit #9512](https://github.com/rdkit/rdkit/pull/9512) — safely representable radical state is preserved across the direct InChI adapter so direct identifier generation agrees with the MolBlock path for the reported single-radical case → **MERGED**

![CONFIG / POLICY ×4](https://img.shields.io/badge/CONFIG%20%2F%20POLICY-4-9a6700?style=flat-square&labelColor=9a6700)

- [bmad-loop #587](https://github.com/bmad-code-org/bmad-loop/pull/587) — strict `limits.*` scalar validation prevents quoted or wrong-type TOML values from silently changing policy meaning → **MERGED**
- [makoto2 #94](https://github.com/pooza/makoto2/pull/94) — service URLs preserve their HTTP(S)-only contract by rejecting misspelled or non-HTTP(S) schemes during configuration validation → **MERGED**
- [Rosetta #284](https://github.com/griddynamics/rosetta/pull/284) — configurable Curiocity turn caps flow through case config and CLI override while preserving the existing 100-turn default → **MERGED**
- [Rosetta #285](https://github.com/griddynamics/rosetta/pull/285) — plan writes reject empty, whitespace-only, and non-string names through shared validation while preserving omitted-name defaults → **MERGED**

![RETRY / RECOVERY ×2](https://img.shields.io/badge/RETRY%20%2F%20RECOVERY-2-1a7f37?style=flat-square&labelColor=1a7f37)

- [Weftmap #178](https://github.com/DataDave-Dev/weftmap/pull/178) — a failed tree-sitter initialization remains a failure for the current caller while clearing the cached promise so a later request can retry → **MERGED**
- [Python Code Health Analyzer #19](https://github.com/Johnkothapalli/python-code-health-analyzer/pull/19) — malformed cached reports recover as cache misses without swallowing SQLite operational failures, then repopulate with valid analysis state → **MERGED**

![INSTALL / COMPLETION ×2](https://img.shields.io/badge/INSTALL%20%2F%20COMPLETION-2-bc4c00?style=flat-square&labelColor=bc4c00)

- [RNAlysis #289](https://github.com/GuyTeichman/RNAlysis/pull/289) — incomplete R-package installation cannot silently continue as if required packages are available → **MERGED**
- [KaotoIO camel-catalog #130](https://github.com/KaotoIO/camel-catalog/pull/130) — catalog generation now fails when an aggregate handler throws instead of silently continuing, while preserving the original failure cause → **MERGED**

![TRANSPORT / PARTIAL PROGRESS ×1](https://img.shields.io/badge/TRANSPORT%20%2F%20PARTIAL%20PROGRESS-1-0e7490?style=flat-square&labelColor=0e7490)

- [Wingfoil #839](https://github.com/wingfoil-io/wingfoil/pull/839) — partial non-blocking FIX/TCP writes; maintainer confirmed the diagnosis and repair before merge → **MERGED**

![NUMERIC / REPRESENTATION ×3](https://img.shields.io/badge/NUMERIC%20%2F%20REPRESENTATION-3-cf222e?style=flat-square&labelColor=cf222e)

- [Apple swift-openapi-generator #939](https://github.com/apple/swift-openapi-generator/pull/939) — duplicate generated schema names fail with a deterministic diagnostic instead of crashing during recursive-type boxing → **MERGED**
- [Sony nmos-cpp #520](https://github.com/sony/nmos-cpp/pull/520) — invalid Node interface port IDs fall back to the existing schema-valid null address; maintainer review requested repository-native regex validation and expanded malformed-input coverage before merge → **MERGED**
- [Gren core #135](https://github.com/gren-lang/core/pull/135) — exact integer parsing at the maximum-safe-number boundary → **MERGED**

These are public OSS contributions, not client engagements or evidence of paid commercial conversion.

## Current work

- [Value-Locked Repository Recovery](https://github.com/shin4141/value-locked-repository-recovery-public)
- [Decision-OS V13 LoopKit](https://github.com/shin4141/decision-os-v13-loopkit)
- [AGENTS.md Compactor](https://github.com/shin4141/agents-md-compactor)

## One bounded boundary first

You do not need to rely on me for every issue.
Start with one consequential boundary.
I aim to leave not only the repair, but also the conditions and checks that help your team or AI recognize the same class of failure next time.

If that proves useful, bring me back for the next consequential boundary.

Private boundary review / repair / research collaboration: [siriusa.paper@gmail.com](mailto:siriusa.paper@gmail.com)
