I investigate and fix failures in how software tracks completion, permissions, and recovery—for example, reporting an operation as done before the requested state exists. I also repair the tests and diagnostics that let these failures go unnoticed.

## Current work

### Sensitive Data Egress Gate

**Design the maximum loss after one credential is compromised.**

If one administrator credential is abused, can it reach 100 records, 10,000, or effectively all of them?

I design bounded data-egress conditions across volume, time, approval, destination, and exception paths.

- [Service and design approach →](https://shin4141.github.io/sensitive-data-egress-gate/)
- [Reference implementation →](https://github.com/shin4141/sensitive-data-egress-gate-reference)

The service page includes a sample deliverable.

**You can commission the design only. Your existing engineers or vendor can implement it internally.**

## Selected upstream repairs

- **[FOSSLight / fosslight_util](https://github.com/fosslight/fosslight_util/pull/319)** — failed log-destination setup could detach the active file handler before the caller could record the failure → the merged fix prepares the destination first, preserving diagnostics and retryability.
- **[Toyota Connected / emb_cli](https://github.com/toyota-connected/emb_cli/pull/240)** — packaging staging spawned `chmod` once per mode-bearing file → the merged fix batches destinations by mode within bounded argv chunks while preserving copy/permission order and failure handling.
- **[Mercedes-Benz / odxtools](https://github.com/mercedes-benz/odxtools/pull/532)** — length-prefixed diagnostic strings mixed UTF-8 byte counts with a different configured encoding → the merged fix uses one encoding consistently for the prefix and payload.
- **[Kakao / actionbase](https://github.com/kakao/actionbase/pull/505)** — an encoding exception could permanently remove a borrowed buffer from the pool → the merged fix returns it in `finally`, and the maintainer invited a follow-up repair.
- **[NIST / mSCP](https://github.com/usnistgov/macos_security/pull/775)** — excluded rules appeared in the JSON manifest → the merged fix omits them; Shin is named in [Release 27.0](https://github.com/usnistgov/macos_security/releases/tag/release_27.0).
- **[Apple / Swift OpenAPI Generator](https://github.com/apple/swift-openapi-generator/pull/939)** — duplicate generated schema names crashed generation → the merged fix emits a deterministic error.
- **[Microsoft / Power Platform provider](https://github.com/microsoft/terraform-provider-power-platform/pull/1254)** — HTTP 409 could report success before the requested state existed → the merged fix checks remote state before declaring success; otherwise it retries.
- **[ESA / pagmo2](https://github.com/esa/pagmo2/pull/634)** — C++20 stateless lambdas broke BFE test assumptions → the merged tests and docs reflect the language change.
- <a id="openssl-adoption-beyond-a-direct-pr-merge"></a>**[OpenSSL](https://github.com/openssl/openssl/pull/32685)** — recursive RAND seed-source construction exhausted the stack → clean failure in a [maintainer-committed repair](https://github.com/openssl/openssl/commit/aeeca5a9e07166183fe323f336c9177a9b524c78).

**39 direct upstream merges across 34 independent public repositories.** OpenSSL's maintainer adoption is listed separately and is not in that total.

[View all upstream contributions →](MERGE_PORTFOLIO.md)

## Projects and contact

Other projects: [Decision-OS V13 LoopKit](https://github.com/shin4141/decision-os-v13-loopkit) · [Value-Locked Repository Recovery](https://github.com/shin4141/value-locked-repository-recovery-public) · [AGENTS.md Compactor](https://github.com/shin4141/agents-md-compactor)

For security design, software review, or repair inquiries: [siriusa.paper@gmail.com](mailto:siriusa.paper@gmail.com)
