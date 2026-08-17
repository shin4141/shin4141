# Shin

Independent researcher and builder working on AI systems, boundary integrity, and Decision-OS.

I focus on consequential state transitions — places where a system says something is complete, settled, authorized, recorded, cancelled, or recovered, but the underlying state does not fully support that claim.

**I don’t just fix the broken point. I repair the transition so the system can move forward without carrying the same failure into its next state.**

Typical boundaries: retry, rollback, replay, partial progress, authority changes, durable state, payment / settlement state, and AI-agent handoff.

## External OSS trust proof

**9 direct upstream merges across 8 independent public repositories**

- [Questboard #151](https://github.com/rictaworks/questboard/pull/151) — existing-member invite state and truthful role visibility → **MERGED**
- [PyScrappy #148](https://github.com/mldsveda/PyScrappy/pull/148) — derived-selector context inheritance; maintainer independently verified the repair locally and confirmed the regression coverage → **MERGED**
- [Gren core #135](https://github.com/gren-lang/core/pull/135) — exact integer parsing at the maximum-safe-number boundary → **MERGED**
- [Weftmap #175](https://github.com/DataDave-Dev/weftmap/pull/175) — stale graph and error invalidation across workspace context changes → **MERGED**
- [makoto2 #56](https://github.com/pooza/makoto2/pull/56) — process-state truth / permission handling; maintainer reproduced the failure and re-verified the repair with real `EACCES` → **MERGED**
- [Job Autofill #215](https://github.com/ritsth/job-autofill-extension/pull/215) — preserve known metadata when blank inputs would otherwise overwrite it → **MERGED**
- [Wingfoil #839](https://github.com/wingfoil-io/wingfoil/pull/839) — partial non-blocking FIX/TCP writes; maintainer confirmed the diagnosis and repair before merge → **MERGED**
- [RNAlysis #289](https://github.com/GuyTeichman/RNAlysis/pull/289) — incomplete R-package installation cannot silently continue as if required packages are available → **MERGED**
- [Job Autofill #221](https://github.com/ritsth/job-autofill-extension/pull/221) — company detection falls back to trimmed image alt text when visible text is absent; visible text retains priority; blank alt values preserve selector fallthrough → **MERGED**

These are public OSS contributions, not client engagements or evidence of paid commercial conversion.

## Current open repair work

These are submitted but not yet counted as merged proof:

- [Vercel Workflow #3575](https://github.com/vercel/workflow/pull/3575) — **SUBMITTED / OPEN / NOT COUNTED AS MERGED PROOF** — materialized state + source-of-truth event atomicity
- [Cerbos #3328](https://github.com/cerbos/cerbos/pull/3328) — **SUBMITTED / OPEN / NOT COUNTED AS MERGED PROOF** — accepted policy mutation != current valid authority chain
- [Mercur #1399](https://github.com/mercurjs/mercur/pull/1399) — **SUBMITTED / OPEN / NOT COUNTED AS MERGED PROOF** — correlated payment evidence != independent financial transitions

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
