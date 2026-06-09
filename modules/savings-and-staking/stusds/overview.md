# stusds

## Codebases

```yaml
repositories:
- id: stusds
  name: stusds
  provider: github
  url: https://github.com/sky-ecosystem/stusds
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/stusds/branch-master"
    checked_out_branch: master
    pinned_commit: 486bfe342c01afab7387a920dfcd7eeaaf91f4b7
```

## Deployments

```yaml
deployments:
- id: st-usds-ethereum
  contract_id: st-usds
  contract_name: StUsds
  status: live
  chain: Ethereum
  address: '0x7A61B7adCFD493f7CF0F86dFCECB94b72c227F22'
  implementation:
    codebase: stusds
    submodule_path: "./codebases/stusds/branch-master"
    source_path: src/StUsds.sol
    contract_name: StUsds
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
- id: st-usds-mom-ethereum
  contract_id: st-usds-mom
  contract_name: StUsdsMom
  status: live
  chain: Ethereum
  address: Address pending to be deployed with latest version
  implementation:
    codebase: stusds
    submodule_path: "./codebases/stusds/branch-master"
    source_path: src/StUsdsMom.sol
    contract_name: StUsdsMom
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
- id: st-usds-rate-setter-ethereum
  contract_id: st-usds-rate-setter
  contract_name: StUsdsRateSetter
  status: live
  chain: Ethereum
  address: '0x30784615252B13E1DbE2bDf598627eaC297Bf4C5'
  implementation:
    codebase: stusds
    submodule_path: "./codebases/stusds/branch-master"
    source_path: src/StUsdsRateSetter.sol
    contract_name: StUsdsRateSetter
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-stusds
  auditor: ChainSecurity
  report_title: Sky stUSDS Audit
  current_version: v2026-04
  versions:
  - id: v2025-08
    reference_refs:
    - chainsecurity-stusds-2025-08
    version_label: August 2025
    status: superseded
    superseded_by: v2026-04
    audited_codebases:
    - stusds
    audited_sources:
    - codebase: stusds
      path: src/StUsds.sol
    - codebase: stusds
      path: src/StUsdsMom.sol
    - codebase: stusds
      path: src/StUsdsRateSetter.sol
    covered_contracts:
    - id: st-usds
      name: StUsds
    - id: st-usds-mom
      name: StUsdsMom
    - id: st-usds-rate-setter
      name: StUsdsRateSetter
  - id: v2026-04
    reference_refs:
    - chainsecurity-stusds-2026-04
    version_label: April 2026
    status: current
    supersedes:
    - v2025-08
    audited_codebases:
    - stusds
    audited_sources:
    - codebase: stusds
      path: src/StUsds.sol
    - codebase: stusds
      path: src/StUsdsMom.sol
    - codebase: stusds
      path: src/StUsdsRateSetter.sol
    covered_contracts:
    - id: st-usds
      name: StUsds
    - id: st-usds-mom
      name: StUsdsMom
    - id: st-usds-rate-setter
      name: StUsdsRateSetter
- id: cantina-stusds
  auditor: Cantina
  report_title: Sky stUSDS Audit
  current_version: v2025-08
  versions:
  - id: v2025-08
    reference_refs:
    - cantina-stusds-2025-08
    version_label: August 2025
    status: current
    audited_codebases:
    - stusds
    audited_sources:
    - codebase: stusds
      path: src/StUsds.sol
    covered_contracts:
    - id: st-usds
      name: StUsds
- id: cantina-stusdsmom
  auditor: Cantina
  report_title: Sky stUSDSMom Audit
  current_version: v2026-05
  versions:
  - id: v2026-05
    reference_refs:
    - cantina-stusdsmom-2026-05
    version_label: May 2026
    status: current
    audited_codebases:
    - stusds
    audited_sources:
    - codebase: stusds
      path: src/StUsdsMom.sol
    covered_contracts:
    - id: st-usds-mom
      name: StUsdsMom
references:
- id: chainsecurity-stusds-2025-08
  type: audit_report
  title: ChainSecurity Sky stUSDS Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/stusds/master/audit/20250812-ChainSecurity_Sky_stUSDS_audit.pdf
  path: audit-reports/chainsecurity-stusds-2025-08.pdf
  date_published: '2025-08-12'
  date_checked: '2026-06-08'
  content_sha256: 48b5c3d0e0cdd7bacfbd0d662d01320c7575bf9483ef947a9252e1c4d4f797a3
- id: chainsecurity-stusds-2026-04
  type: audit_report
  title: ChainSecurity Sky SkyStUSDS Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/stusds/master/audit/20260410-ChainSecurity_Sky_SkyStUSDS_Audit.pdf
  path: audit-reports/chainsecurity-stusds-2026-04.pdf
  date_published: '2026-04-10'
  date_checked: '2026-06-08'
  content_sha256: ff71c993cae6f8f7ec5cd62fe424fff8e8ea721a565f7bf29e6f89331c143eb6
- id: cantina-stusds-2025-08
  type: audit_report
  title: Cantina Sky stUSDS Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/stusds/master/audit/20250818-cantina-report-sky-stusds.pdf
  path: audit-reports/cantina-stusds-2025-08.pdf
  date_published: '2025-08-18'
  date_checked: '2026-06-08'
  content_sha256: 5ce80f7ff85f119c051b61f8fccf95b4b1dd25da06b38518bd8b39e5d9933e8e
- id: cantina-stusdsmom-2026-05
  type: audit_report
  title: Cantina Sky stUSDSMom Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/stusds/master/audit/20260504-cantina-report-sky-stusdsmom.pdf
  path: audit-reports/cantina-stusdsmom-2026-05.pdf
  date_published: '2026-05-04'
  date_checked: '2026-06-08'
  content_sha256: deeb9d7d70a0cd3991207688b53da1600b23e6274dd7bc4294b503fdadbe7497
```
