# V216 profile change record

Before this change, `shin4141/shin4141` main was `cc3e38fb2cb4fc3ba339050d30fe1deef9acc425` and `README.md` had SHA-256 `a5b6c81419e1f0176aaaf62edebaf0276f2b025b861bdf1f31dcec0227dcf312`.

The approved V216 prototype was PR [decision-os-v13-loopkit #172](https://github.com/shin4141/decision-os-v13-loopkit/pull/172), head `a3c3e6633b13684adc08beab28883a57b11d5cbb`, admitted on V13 main as `94e106701e29a6eadfac132a6b7cb0d0907d909f`. This profile change substitutes a picture heading and inserts one compact animated GIF after the opening paragraph. The rest of the profile text and the user's GitHub account avatar are not changed. The image URLs use the fixed V13 main commit, not a work branch.

Rollback: use a new reviewed profile change to restore the heading line and remove the inserted GIF, taking the exact prior `README.md` from `cc3e38f` as the comparison source. Do not reset a later main or overwrite unrelated later profile edits. The V13 asset commit and merged PR remain available even if the live profile later uses a different image source.
