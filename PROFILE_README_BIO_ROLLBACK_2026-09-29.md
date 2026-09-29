# Profile README and bio change record — 2026-09-29

The profile repository's public `main` before this prose update was `8dae0fc1a47ba6153de6214f588192bf18a30986`. Its `README.md` SHA-256 was `0daf7b028bb887b5f05f70881127b83b55109d6b6ffcb47fd1588079c27119b6`. The exact prior README is available with `git show 8dae0fc1a47ba6153de6214f588192bf18a30986:README.md`.

The prior GitHub account bio was:

> Decision-OS researcher & builder. Governed multi-agent workflows for restartability, handoff integrity, role separation, and evidence-bound release.

To roll back, create a new reviewed profile PR that restores the desired prose from that commit while preserving any newer `profile-motion:begin` / `profile-motion:end` block and image query hashes from the then-current `main`. Restore the bio with the exact text above through the GitHub profile settings or API. Do not reset `main` or replace a later daily GIF update. `MERGE_PORTFOLIO.md` and the daily refresh workflow were not changed by this prose update.
