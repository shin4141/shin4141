# V216 profile change record

Before this change, `shin4141/shin4141` main was `cc3e38fb2cb4fc3ba339050d30fe1deef9acc425` and `README.md` had SHA-256 `a5b6c81419e1f0176aaaf62edebaf0276f2b025b861bdf1f31dcec0227dcf312`.

The approved V216 prototype was PR [decision-os-v13-loopkit #172](https://github.com/shin4141/decision-os-v13-loopkit/pull/172), head `a3c3e6633b13684adc08beab28883a57b11d5cbb`, admitted on V13 main as `94e106701e29a6eadfac132a6b7cb0d0907d909f`. This profile change substitutes a picture heading and inserts one compact animated GIF after the opening paragraph. The rest of the profile text and the user's GitHub account avatar are not changed. The image URLs use the fixed V13 main commit, not a work branch.

Rollback: use a new reviewed profile change to restore the heading line and remove the inserted GIF, taking the exact prior `README.md` from `cc3e38f` as the comparison source. Do not reset a later main or overwrite unrelated later profile edits. The V13 asset commit and merged PR remain available even if the live profile later uses a different image source.

## Independent repository handoff

The first profile update landed as `e5d3b94ddb2ca88be760115120761b45c0612491`. After the generator was extracted, [github-profile-motion](https://github.com/shin4141/github-profile-motion) main at `af863aca4595b32e18e05fda19a2e3cbda385463` became the image source and the README gained one usage link. This second update changes only those three image URLs and adds that link. For a narrow rollback of the source switch, restore the three V13 image URLs from `e5d3b94` in a new reviewed commit and remove the usage link; retain later unrelated edits. For a complete presentation rollback, use the pre-V216 comparison source above. Both asset commits are immutable recovery points.

## Compact profile follow-up

Before the compacting edit, profile main was `5cc31383b3760320359d6e7938a6af60fd039df3` and `README.md` SHA-256 was `af9814f72552f30dbc16f4030b0a90c0fe4b40b3b8ad132e9ba50e4fe390dbe6`. The fixed image URLs, account avatar, 32-direct-merge ledger, and contact address are not changed. The cat GIF at independent-repository commit `af863aca4595b32e18e05fda19a2e3cbda385463` exactly regenerates from `cat.json` and `shin_activity_2026-09-20.json` with seed 216; that JSON identifies `shin4141`, GitHub GraphQL `contributionsCollection`, observation `2026-09-20T02:47:24Z`, and days `2026-03-08` through `2026-09-20`.

Rollback the compacting edit by creating a new reviewed profile PR that uses `5cc3138:README.md` as the full prior-state comparison, or restores selected passages from it. Do not reset a later main or overwrite unrelated later edits. The detailed direct-merge evidence stays in `MERGE_PORTFOLIO.md`; the OpenSSL adoption distinction remains visible in the compact README and at the pre-edit commit.

## Daily real-data refresh

Shin authorized a once-daily and manual GitHub Actions refresh. Before this change, profile main was `1f76c9d9db0def201779f13e1a1afcfd6ac0ca2c`, `README.md` SHA-256 was `c3b0f94b7e18443db7263b790687a6b019d15cb64234049ee75e7c6923b2083f`, and the GIF URL referred to immutable generator commit `af863aca4595b32e18e05fda19a2e3cbda385463`. The same approved cat sprites and exact GIF are copied here as the initial fallback. The workflow calls generator commit `f52dfa0d3ab1c224904bb2662d37f77911b0225c`, captures `shin4141` via authenticated GitHub GraphQL, renders the same two-scene pattern, then commits a new `profile-motion.gif` and a hash-versioned README URL together only after validation. The fixed heading, short profile prose, evidence classifications, portfolio and contact are untouched. Schedule: 03:17 UTC daily plus manual dispatch; the schedule being present is not proof of a scheduled success.

Rollback: disable or remove `.github/workflows/update-profile-motion.yml` first, so another scheduled run cannot reapply the change. Then use a new reviewed PR to restore the previous caption and fixed image URL from `1f76c9d:README.md`. The last generated GIF can remain as a historical file or be removed by that reviewed change; do not reset a later main. If a run fails, the previous **remote** GIF/README remain live, the Actions run is visibly failed, and there is no synthetic fallback. The separate generator repository has its own [rollout and rollback record](https://github.com/shin4141/github-profile-motion/blob/main/DAILY_REFRESH_ROLLOUT.md).
