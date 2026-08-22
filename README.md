# Shin

Independent researcher and builder working on AI systems, boundary integrity, and Decision-OS.

I focus on consequential state transitions — places where a system says something is complete, settled, authorized, recorded, cancelled, or recovered, but the underlying state does not fully support that claim.

**I don’t just fix the broken point. I repair the transition so the system can move forward without carrying the same failure into its next state.**

Typical boundaries: retry, rollback, replay, partial progress, authority changes, durable state, payment / settlement state, and AI-agent handoff.

## External OSS trust proof

### Featured upstream merges

> **[Apple / swift-openapi-generator #939](https://github.com/apple/swift-openapi-generator/pull/939)** — duplicate generated schema-name collisions now produce a deterministic diagnostic instead of crashing the generator; regression coverage included → **MERGED**

> **[Sony / nmos-cpp #520](https://github.com/sony/nmos-cpp/pull/520)** — invalid Node interface port IDs now fall back to the existing schema-valid representation; maintainer review drove regex-based validation and expanded malformed-input coverage before merge → **MERGED**

**21 direct upstream merges across 17 independent public repositories**

![STATE / TRANSITION ×5](https://img.shields.io/badge/STATE%20%2F%20TRANSITION-5-1f6feb?style=flat-square&labelColor=1f6feb) ![DATA / CONTEXT ×4](https://img.shields.io/badge/DATA%20%2F%20CONTEXT-4-8250df?style=flat-square&labelColor=8250df) ![CONFIG / POLICY ×4](https://img.shields.io/badge/CONFIG%20%2F%20POLICY-4-9a6700?style=flat-square&labelColor=9a6700) ![RETRY / RECOVERY ×2](https://img.shields.io/badge/RETRY%20%2F%20RECOVERY-2-1a7f37?style=flat-square&labelColor=1a7f37) ![INSTALL / COMPLETION ×2](https://img.shields.io/badge/INSTALL%20%2F%20COMPLETION-2-bc4c00?style=flat-square&labelColor=bc4c00) ![TRANSPORT / PARTIAL PROGRESS ×1](https://img.shields.io/badge/TRANSPORT%20%2F%20PARTIAL%20PROGRESS-1-0e7490?style=flat-square&labelColor=0e7490) ![NUMERIC / REPRESENTATION ×3](https://img.shields.io/badge/NUMERIC%20%2F%20REPRESENTATION-3-cf222e?style=flat-square&labelColor=cf222e)

![STATE / TRANSITION ×5](https://img.shields.io/badge/STATE%20%2F%20TRANSITION-5-1f6feb?style=flat-square&labelColor=1f6feb)

- [Questboard #151](https://github.com/rictaworks/questboard/pull/151) — existing-member invite state and truthful role visibility → **MERGED**
- [Weftmap #175](https://github.com/DataDave-Dev/weftmap/pull/175) — stale graph and error invalidation across workspace context changes → **MERGED**
- [makoto2 #56](https://github.com/pooza/makoto2/pull/56) — process-state truth / permission handling; maintainer reproduced the failure and re-verified the repair with real `EACCES` → **MERGED**
- [Codesema #32](https://github.com/getCodesema/codesema-cli/pull/32) — renamed and copied preview entries retain the destination path used for later status and diff lookup → **MERGED**
- [Mercur #1399](https://github.com/mercurjs/mercur/pull/1399) — terminal payment evidence is counted once so fully captured/refunded collections do not collapse into false partial states → **MERGED**

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

## Current open repair work

These are submitted but not yet counted as merged proof:

- [Vercel Workflow #3575](https://github.com/vercel/workflow/pull/3575) — **SUBMITTED / OPEN / NOT COUNTED AS MERGED PROOF** — materialized state + source-of-truth event atomicity

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
