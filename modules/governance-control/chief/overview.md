# chief

## Codebases

```yaml
repositories:
- id: chief
  name: chief
  provider: github
  url: https://github.com/sky-ecosystem/chief
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/chief/branch-master"
    checked_out_branch: master
    pinned_commit: ed7f9129319ee11d79f5d9948e0f7fce7e4dfeff
```

## Deployments

```yaml
deployments:
- id: chief-ethereum
  contract_id: chief
  contract_name: Chief
  status: live
  chain: Ethereum
  address: '0x929d9A1435662357F54AdcF64DcEE4d6b867a6f9'
  implementation:
    codebase: chief
    submodule_path: "./codebases/chief/branch-master"
    source_path: src/Chief.sol
    contract_name: Chief
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-chief
  auditor: ChainSecurity
  report_title: Sky Chief Audit
  current_version: v2025-03
  versions:
  - id: v2025-03
    reference_refs:
    - chainsecurity-chief-2025-03
    version_label: March 2025
    status: current
    audited_codebases:
    - chief
    audited_sources:
    - codebase: chief
      path: src/Chief.sol
    covered_contracts:
    - id: chief
      name: Chief
- id: cantina-chief
  auditor: Cantina
  report_title: Sky Chief Audit
  current_version: v2025-04
  versions:
  - id: v2025-04
    reference_refs:
    - cantina-chief-2025-04
    version_label: April 2025
    status: current
    audited_codebases:
    - chief
    audited_sources:
    - codebase: chief
      path: src/Chief.sol
    covered_contracts:
    - id: chief
      name: Chief
references:
- id: chainsecurity-chief-2025-03
  type: audit_report
  title: ChainSecurity Sky Chief Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/chief/master/audit/20250321-ChainSecurity_Sky_Chief_audit.pdf
  path: audit-reports/chainsecurity-chief-2025-03.pdf
  date_published: '2025-03-21'
  date_checked: '2026-06-08'
  content_sha256: 2781defec71ec5e966c740a5a8c04de83ff7d666a8b06a7a41c10861be13807e
- id: cantina-chief-2025-04
  type: audit_report
  title: Cantina Sky Chief Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/chief/master/audit/20250430-cantina-report-sky-chief.pdf
  path: audit-reports/cantina-chief-2025-04.pdf
  date_published: '2025-04-30'
  date_checked: '2026-06-08'
  content_sha256: dbfa61692057e491ecd67ef9c6025ed9147e63207a4d3068475b82d398107db6
```
