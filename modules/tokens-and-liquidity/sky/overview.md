# sky

## Codebases

```yaml
repositories:
- id: sky
  name: sky
  provider: github
  url: https://github.com/sky-ecosystem/sky
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/sky/branch-master"
    checked_out_branch: master
    pinned_commit: db6687a5e8dca8de1f3e86887d6ab5b66921b9af
```

## Deployments

```yaml
deployments:
- id: sky-ethereum
  contract_id: sky
  contract_name: Sky
  status: live
  chain: Ethereum
  address: '0x56072C95FAA701256059aa122697B133aDEd9279'
  implementation:
    codebase: sky
    submodule_path: "./codebases/sky/branch-master"
    source_path: src/Sky.sol
    contract_name: Sky
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
- id: mkr-sky-ethereum
  contract_id: mkr-sky
  contract_name: MkrSky
  status: live
  chain: Ethereum
  address: '0xA1Ea1bA18E88C381C724a75F23a130420C403f9a'
  implementation:
    codebase: sky
    submodule_path: "./codebases/sky/branch-master"
    source_path: src/MkrSky.sol
    contract_name: MkrSky
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-sky
  auditor: ChainSecurity
  report_title: Sky Audit
  current_version: v2025-04
  versions:
  - id: v2025-04
    reference_refs:
    - chainsecurity-sky-2025-04
    version_label: April 2025
    status: current
    audited_codebases:
    - sky
    audited_sources:
    - codebase: sky
      path: src/Sky.sol
    - codebase: sky
      path: src/MkrSky.sol
    covered_contracts:
    - id: sky
      name: Sky
    - id: mkr-sky
      name: MkrSky
- id: cantina-sky
  auditor: Cantina
  report_title: Sky Audit Updates
  current_version: v2025-04
  versions:
  - id: v2025-04
    reference_refs:
    - cantina-sky-2025-04
    version_label: April 2025
    status: current
    audited_codebases:
    - sky
    audited_sources:
    - codebase: sky
      path: src/Sky.sol
    - codebase: sky
      path: src/MkrSky.sol
    covered_contracts:
    - id: sky
      name: Sky
    - id: mkr-sky
      name: MkrSky
references:
- id: chainsecurity-sky-2025-04
  type: audit_report
  title: ChainSecurity Sky Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/sky/master/audit/20250416-ChainSecurity_Sky_Sky_audit.pdf
  path: audit-reports/chainsecurity-sky-2025-04.pdf
  date_published: '2025-04-16'
  date_checked: '2026-06-08'
  content_sha256: e44b7e902f8e81fcc0d37f90202db054e84401934208abfb3b8d7b8731d339e9
- id: cantina-sky-2025-04
  type: audit_report
  title: Cantina Sky Audit Updates
  url: https://raw.githubusercontent.com/sky-ecosystem/sky/master/audit/20250430-cantina-report-sky-sky-updates.pdf
  path: audit-reports/cantina-sky-2025-04.pdf
  date_published: '2025-04-30'
  date_checked: '2026-06-08'
  content_sha256: 6615daefb621eb93a770b9a9b254bd76ad0e70dc95ce4d74f64a231e71adf8b6
```
