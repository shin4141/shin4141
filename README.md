I repair software boundary failures where systems report the wrong state, retain the wrong authority, or cannot recover cleanly after failure.

**[39 direct upstream merges across 34 independent public repositories](MERGE_PORTFOLIO.md)** — including Apple, Microsoft, NIST, Kakao, Mercedes-Benz, ESA, Hyperledger, and others.

Typical failures I work on:

- **Completion** — a system reports success before the requested state actually exists.
- **Authority** — permissions, policy, or access survive beyond the boundary where they should end.
- **Recovery** — failure leaves stale state, lost diagnostics, or a broken retry path.

**If your system has one of these failure modes, send me the failing path or reproduction:** [siriusa.paper@gmail.com](mailto:siriusa.paper@gmail.com)

## Selected upstream repairs

### State / completion truth

- **[Microsoft / Power Platform provider](https://github.com/microsoft/terraform-provider-power-platform/pull/1254)** — HTTP 409 could report success before the requested remote state existed → the merged fix checks remote state before declaring success; otherwise it retries.

### Authority / policy boundaries

- **[Rundeck](https://github.com/rundeck/rundeck/pull/10488)** — project import permission could allow configuration changes without `configure` authorization → the merged fix requires both permissions for configuration imports.
- **[NIST / mSCP](https://github.com/usnistgov/macos_security/pull/775)** — excluded rules appeared in the JSON manifest → the merged fix omits them; Shin is named in [Release 27.0](https://github.com/usnistgov/macos_security/releases/tag/release_27.0).

### Recovery / failure integrity

- **[Kakao / actionbase](https://github.com/kakao/actionbase/pull/505)** — an encoding exception could permanently remove a borrowed buffer from the pool → the merged fix returns it in `finally`, preserving later reuse.
- **[FOSSLight / fosslight_util](https://github.com/fosslight/fosslight_util/pull/319)** — failed log-destination setup could detach the active file handler before the caller could record the failure → the merged fix prepares the destination first, preserving diagnostics and retryability.
- <a id="openssl-adoption-beyond-a-direct-pr-merge"></a>**[OpenSSL](https://github.com/openssl/openssl/pull/32685)** — recursive RAND seed-source construction exhausted the stack → clean failure in a [maintainer-committed repair](https://github.com/openssl/openssl/commit/aeeca5a9e07166183fe323f336c9177a9b524c78).

OpenSSL's maintainer adoption is excluded from the direct merge total.

### Representation / boundary consistency

- **[Mercedes-Benz / odxtools](https://github.com/mercedes-benz/odxtools/pull/532)** — length-prefixed diagnostic strings mixed UTF-8 byte counts with a different configured encoding → the merged fix uses one encoding consistently for the prefix and payload.
- **[Apple / Swift OpenAPI Generator](https://github.com/apple/swift-openapi-generator/pull/939)** — duplicate generated schema names crashed generation → the merged fix emits a deterministic error.

<details>
<summary>Additional upstream evidence</summary>

- **[ESA / pagmo2](https://github.com/esa/pagmo2/pull/634)** — C++20 stateless lambdas broke BFE test assumptions → the merged tests and docs reflect the language change.
- **[Hyperledger Besu](https://github.com/besu-eth/besu/pull/11128)** — ordinary `state-test --json` mixed a human summary into JSONL → the merged fix keeps that output machine-readable.
- **[Toyota Connected / emb_cli](https://github.com/toyota-connected/emb_cli/pull/240)** — packaging staging spawned `chmod` once per mode-bearing file → the merged fix batches destinations by mode within bounded argv chunks while preserving copy/permission order and failure handling.

</details>

[View all upstream contributions →](MERGE_PORTFOLIO.md)

## Applied work

### Sensitive Data Egress Gate

Applying the same boundary-repair approach to bounded data loss after credential compromise.

**Design the maximum loss after one credential is compromised.**

If one administrator credential is abused, can it reach 100 records, 10,000, or effectively all of them?

I design bounded data-egress conditions across volume, time, approval, destination, and exception paths.

This work is relevant to questions such as **personal data security design**, **maximum data extraction after credential compromise**, **one-credential blast radius**, **AI agent data egress**, and **stop / approval / recovery boundaries** for systems that can access customer or sensitive data.

- [Service and design approach →](https://shin4141.github.io/sensitive-data-egress-gate/)
- [Reference implementation →](https://github.com/shin4141/sensitive-data-egress-gate-reference)

The service page includes a sample deliverable.

**You can commission the design only. Your existing engineers or vendor can implement it internally.**

## Projects and contact

Other projects: [Decision-OS V13 LoopKit](https://github.com/shin4141/decision-os-v13-loopkit) · [Value-Locked Repository Recovery](https://github.com/shin4141/value-locked-repository-recovery-public) · [AGENTS.md Compactor](https://github.com/shin4141/agents-md-compactor)

Contact: [siriusa.paper@gmail.com](mailto:siriusa.paper@gmail.com)
