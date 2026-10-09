<p><a href="MERGE_PORTFOLIO.md"><picture><source media="(max-width: 600px)" srcset="./assets/hero-mobile.svg"><img src="./assets/hero.svg" alt="Fixing failures across software boundaries. Reproduced. Repaired. Reviewed upstream. 39 direct upstream merges across 34 independent public repositories." width="1200"></picture></a></p>

<p><a id="organization-proof-wall"></a><a id="merged-upstream"></a>
<a href="https://github.com/apple/swift-openapi-generator/pull/939"><img src="./assets/org-apple.svg" width="144" alt="Apple — Swift OpenAPI Generator. MERGED PR #939 in apple/swift-openapi-generator."></a>
<a href="https://github.com/microsoft/terraform-provider-power-platform/pull/1254"><img src="./assets/org-microsoft.svg" width="144" alt="Microsoft — Power Platform provider. MERGED PR #1254 in microsoft/terraform-provider-power-platform."></a>
<a href="https://github.com/sony/nmos-cpp/pull/520"><img src="./assets/org-sony.svg" width="144" alt="Sony — nmos-cpp media networking. MERGED PR #520 in sony/nmos-cpp."></a>
<a href="https://github.com/usnistgov/macos_security/pull/775"><img src="./assets/org-nist.svg" width="144" alt="NIST — macOS Security Compliance Project. MERGED PR #775 in usnistgov/macos_security."></a>
<a href="https://github.com/mercedes-benz/odxtools/pull/532"><img src="./assets/org-mercedes.svg" width="144" alt="Mercedes-Benz — odxtools automotive diagnostics. MERGED PR #532 in mercedes-benz/odxtools."></a>
<a href="https://github.com/fosslight/fosslight_util/pull/319"><img src="./assets/org-fosslight.svg" width="144" alt="LG Electronics — FOSSLight Util. MERGED PR #319 in fosslight/fosslight_util."></a>
<a href="https://github.com/besu-eth/besu/pull/11128"><img src="./assets/org-besu.svg" width="144" alt="Ethereum ecosystem — Besu Ethereum client. MERGED PR #11128 in besu-eth/besu."></a>
<a href="https://github.com/anza-xyz/kit/pull/1971"><img src="./assets/org-anza.svg" width="144" alt="Solana ecosystem — Solana Kit SDK by Anza. MERGED PR #1971 in anza-xyz/kit."></a>
<a href="https://github.com/vercel/workflow/pull/3575"><img src="./assets/org-vercel.svg" width="144" alt="Vercel — Workflow SDK. MERGED PR #3575 in vercel/workflow."></a>
<a href="https://github.com/kakao/actionbase/pull/505"><img src="./assets/org-kakao.svg" width="144" alt="Kakao — actionbase interaction database. MERGED PR #505 in kakao/actionbase."></a>
<a href="https://github.com/esa/pagmo2/pull/634"><img src="./assets/org-esa.svg" width="144" alt="European Space Agency (ESA) — pagmo2 scientific optimization. MERGED PR #634 in esa/pagmo2."></a>
<a href="https://github.com/Adyen/adyen-node-api-library/pull/1760"><img src="./assets/org-adyen.svg" width="144" alt="Adyen — Node.js payments API library. MERGED PR #1760 in Adyen/adyen-node-api-library."></a>
<a href="https://github.com/toyota-connected/emb_cli/pull/240"><img src="./assets/org-toyota.svg" width="144" alt="Toyota Connected — emb_cli embedded Linux tooling. MERGED PR #240 in toyota-connected/emb_cli."></a>
<a href="https://github.com/FHIR/sushi/pull/1635"><img src="./assets/org-fhir.svg" width="144" alt="HL7 FHIR ecosystem — SUSHI compiler. MERGED PR #1635 in FHIR/sushi."></a>
<a href="https://github.com/rdkit/rdkit/pull/9512"><img src="./assets/org-rdkit.svg" width="144" alt="RDKit — chemistry toolkit. MERGED PR #9512 in rdkit/rdkit."></a>
<a href="https://github.com/OSC/ondemand/pull/5725"><img src="./assets/org-osc.svg" width="144" alt="Ohio Supercomputer Center — Open OnDemand supercomputing portal. MERGED PR #5725 in OSC/ondemand."></a>
<a href="https://github.com/rundeck/rundeck/pull/10488"><img src="./assets/org-rundeck.svg" width="144" alt="PagerDuty — Rundeck runbook automation. MERGED PR #10488 in rundeck/rundeck."></a>
<a href="https://github.com/WorksApplications/sudachi.rs/pull/360"><img src="./assets/org-sudachi.svg" width="144" alt="Works Applications — Sudachi Japanese text analysis. MERGED PR #360 in WorksApplications/sudachi.rs."></a>
<a href="https://github.com/PowerGridModel/power-grid-model/pull/1547"><img src="./assets/org-pgm.svg" width="144" alt="Linux Foundation energy ecosystem — Power Grid Model / LF Energy. MERGED PR #1547 in PowerGridModel/power-grid-model."></a>
<a href="https://github.com/dynawo/dyn-grid-compliance-verification/pull/385"><img src="./assets/org-dynawo.svg" width="144" alt="Dynawo / DyCoV — power-grid compliance tools. MERGED PR #385 in dynawo/dyn-grid-compliance-verification."></a>
<a href="https://github.com/KaotoIO/camel-catalog/pull/130"><img src="./assets/org-kaoto.svg" width="144" alt="Apache Camel ecosystem — Kaoto integration tooling. MERGED PR #130 in KaotoIO/camel-catalog."></a>
</p>

<p><a id="openssl-adoption-beyond-a-direct-pr-merge"></a><a href="https://github.com/openssl/openssl/commit/aeeca5a9e07166183fe323f336c9177a9b524c78"><img src="./assets/org-openssl-adopted.svg" width="144" alt="OpenSSL — MAINTAINER ADOPTED; commit aeeca5a. Excluded from the 39 direct merges."></a></p>

OpenSSL: maintainer-committed adoption, separate from the direct merge count.

I repair software boundary failures where systems report the wrong state, retain the wrong authority, or cannot recover cleanly after failure.

**[39 direct upstream merges across 34 independent public repositories](MERGE_PORTFOLIO.md)**

**If your system has one of these failure modes, send me the failing path or reproduction:** [siriusa.paper@gmail.com](mailto:siriusa.paper@gmail.com)

## Failure classes<a id="proof-wall"></a><a id="selected-upstream-repairs"></a>

Typical failures I work on:

- **Completion** — a system reports success before the requested state actually exists.
- **Authority** — permissions, policy, or access survive beyond the boundary where they should end.
- **Recovery** — failure leaves stale state, lost diagnostics, or a broken retry path.

<details>
<summary><a id="state--completion-truth"></a><strong>State / completion truth</strong></summary>

- **[Microsoft / Power Platform provider](https://github.com/microsoft/terraform-provider-power-platform/pull/1254)** — HTTP 409 could report success before the requested remote state existed → the merged fix checks remote state before declaring success; otherwise it retries.

</details>

<details>
<summary><a id="authority--policy-boundaries"></a><strong>Authority / policy boundaries</strong></summary>

- **[Rundeck](https://github.com/rundeck/rundeck/pull/10488)** — project import permission could allow configuration changes without `configure` authorization → the merged fix requires both permissions for configuration imports.
- **[NIST / mSCP](https://github.com/usnistgov/macos_security/pull/775)** — excluded rules appeared in the JSON manifest → the merged fix omits them; Shin is named in [Release 27.0](https://github.com/usnistgov/macos_security/releases/tag/release_27.0).

</details>

<details>
<summary><a id="recovery--failure-integrity"></a><strong>Recovery / failure integrity</strong></summary>

- **[Kakao / actionbase](https://github.com/kakao/actionbase/pull/505)** — an encoding exception could permanently remove a borrowed buffer from the pool → the merged fix returns it in `finally`, preserving later reuse.
- **[FOSSLight / fosslight_util](https://github.com/fosslight/fosslight_util/pull/319)** — failed log-destination setup could detach the active file handler before the caller could record the failure → the merged fix prepares the destination first, preserving diagnostics and retryability.
- **[OpenSSL](https://github.com/openssl/openssl/pull/32685)** — recursive RAND seed-source construction exhausted the stack → clean failure in a [maintainer-committed repair](https://github.com/openssl/openssl/commit/aeeca5a9e07166183fe323f336c9177a9b524c78).


</details>

<details>
<summary><a id="representation--boundary-consistency"></a><strong>Representation / boundary consistency</strong></summary>

- **[Mercedes-Benz / odxtools](https://github.com/mercedes-benz/odxtools/pull/532)** — length-prefixed diagnostic strings mixed UTF-8 byte counts with a different configured encoding → the merged fix uses one encoding consistently for the prefix and payload.
- **[Apple / Swift OpenAPI Generator](https://github.com/apple/swift-openapi-generator/pull/939)** — duplicate generated schema names crashed generation → the merged fix emits a deterministic error.

</details>

<details>
<summary>Additional upstream evidence</summary>

- **[ESA / pagmo2](https://github.com/esa/pagmo2/pull/634)** — C++20 stateless lambdas broke BFE test assumptions → the merged tests and docs reflect the language change.
- **[Hyperledger Besu](https://github.com/besu-eth/besu/pull/11128)** — ordinary `state-test --json` mixed a human summary into JSONL → the merged fix keeps that output machine-readable.
- **[Toyota Connected / emb_cli](https://github.com/toyota-connected/emb_cli/pull/240)** — packaging staging spawned `chmod` once per mode-bearing file → the merged fix batches destinations by mode within bounded argv chunks while preserving copy/permission order and failure handling.

</details>

[View all upstream contributions →](MERGE_PORTFOLIO.md)

<details>
<summary><strong>APPROVED / OPEN — pending contributions, not merged</strong></summary>

- [Apache / Jena #4314](https://github.com/apache/jena/pull/4314) — **APPROVED**
- [NVIDIA / GPU Operator #3028](https://github.com/NVIDIA/gpu-operator/pull/3028) — **OPEN**
- [Django / Cookie messages #22085](https://github.com/django/django/pull/22085) — **OPEN**
- [Adobe / Magento / Magento 2 #41430](https://github.com/magento/magento2/pull/41430) — **OPEN**
- [Siemens / Industrial Experience #2862](https://github.com/siemens/ix/pull/2862) — **OPEN**
- [Panasonic / Connect / Teams hook #188](https://github.com/PanasonicConnect/notify-teams-workflows-webhook/pull/188) — **OPEN**
- [Universal Robots / ROS 2 Driver #2013](https://github.com/UniversalRobots/Universal_Robots_ROS2_Driver/pull/2013) — **OPEN**
- [Universal Robots / Client Library #588](https://github.com/UniversalRobots/Universal_Robots_Client_Library/pull/588) — **OPEN**
- [Kakao / actionbase / pool #506](https://github.com/kakao/actionbase/pull/506) — **OPEN**
- [NAVER / Fixture Monkey #1349](https://github.com/naver/fixture-monkey/pull/1349) — **OPEN**
- [Samsung / TizenRT #7549](https://github.com/Samsung/TizenRT/pull/7549) — **OPEN**
- [Metabase / Analytics platform #80783](https://github.com/metabase/metabase/pull/80783) — **OPEN**
- [NASA JPL / Explorer-1 #892](https://github.com/nasa-jpl/explorer-1/pull/892) — **OPEN**
- [CERN ROOT / Cling #568](https://github.com/root-project/cling/pull/568) — **OPEN**
- [NII Cloud Ops / nbsearch #76](https://github.com/NII-cloud-operation/nbsearch/pull/76) — **OPEN**
- [Keycloak / Identity platform #51749](https://github.com/keycloak/keycloak/pull/51749) — **OPEN**
- [AWS Samples / Customer data lake #330](https://github.com/aws-samples/sample-voice-of-customer-datalake/pull/330) — **OPEN**
- [Temporal / Deputy / experimental #314](https://github.com/temporalio/deputy/pull/314) — **OPEN**

</details>

## Applied work

### Sensitive Data Egress Gate

Applying the same boundary-repair approach to bounded data loss after credential compromise.

**Design the maximum loss after one credential is compromised.**

If one administrator credential is abused, can it reach 100 records, 10,000, or effectively all of them?

I design bounded data-egress conditions across volume, time, approval, destination, and exception paths.


- [Service and design approach →](https://shin4141.github.io/sensitive-data-egress-gate/)
- [Reference implementation →](https://github.com/shin4141/sensitive-data-egress-gate-reference)

The service page includes a sample deliverable.

**You can commission the design only. Your existing engineers or vendor can implement it internally.**

## Projects and contact

Other projects: [Decision-OS V13 LoopKit](https://github.com/shin4141/decision-os-v13-loopkit) · [Value-Locked Repository Recovery](https://github.com/shin4141/value-locked-repository-recovery-public) · [AGENTS.md Compactor](https://github.com/shin4141/agents-md-compactor)

Contact: [siriusa.paper@gmail.com](mailto:siriusa.paper@gmail.com)
