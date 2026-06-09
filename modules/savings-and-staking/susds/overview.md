# susds

## Codebases

```yaml
repositories:
- id: sdai
  name: sdai
  provider: github
  url: https://github.com/sky-ecosystem/sdai
  ref: susds
  ref_type: branch
  source_code_roots:
  - src
  - src/l2
  checkout:
    submodule_path: "./branch-susds"
    checked_out_branch: susds
    pinned_commit: dfc7f41cb7599afcb0f0eb1ddaadbf9dd4015dce
```

## Deployments

```yaml
deployments:
- id: s-usds-ethereum
  contract_id: s-usds
  contract_name: SUsds
  status: live
  chain: Ethereum
  address: '0x4e7991e5C547ce825BdEb665EE14a3274f9F61e0'
  implementation:
    codebase: sdai
    submodule_path: "./branch-susds"
    source_path: src/SUsds.sol
    contract_name: SUsds
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
deployment_gaps:
- contract_id: s-usds-l2
  contract_name: SUsds (L2)
  implementation:
    codebase: sdai
    submodule_path: "./branch-susds"
    source_path: src/l2/SUsds.sol
    contract_name: SUsds (L2)
    compiler:
      version: 0.8.21
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-susds
  auditor: ChainSecurity
  report_title: MakerDAO Savings USDS Audit
  current_version: v2024-09
  versions:
  - id: v2024-09
    reference_refs:
    - chainsecurity-susds-2024-09
    version_label: September 2024
    status: current
    audited_codebases:
    - sdai
    audited_sources:
    - codebase: sdai
      path: src/SUsds.sol
    - codebase: sdai
      path: src/l2/SUsds.sol
    covered_contracts:
    - id: s-usds
      name: SUsds
    - id: s-usds-l2
      name: SUsds (L2)
- id: cantina-susds
  auditor: Cantina
  report_title: MakerDAO sUSDS Audit
  current_version: v2024-09
  versions:
  - id: v2024-09
    reference_refs:
    - cantina-susds-2024-09
    version_label: September 2024
    status: current
    audited_codebases:
    - sdai
    audited_sources:
    - codebase: sdai
      path: src/SUsds.sol
    - codebase: sdai
      path: src/l2/SUsds.sol
    covered_contracts:
    - id: s-usds
      name: SUsds
    - id: s-usds-l2
      name: SUsds (L2)
references:
- id: chainsecurity-susds-2024-09
  type: audit_report
  title: ChainSecurity MakerDAO Savings USDS Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/sdai/susds/audit/20240930-ChainSecurity_MakerDAO_Savings_USDS_audit.pdf
  path: audit-reports/chainsecurity-susds-2024-09.pdf
  date_published: '2024-09-30'
  date_checked: '2026-06-08'
  content_sha256: 5a3903cb7bbbae1c71a5aaefa58b0fcb8156ccecc0dd510490de4e52625709f5
- id: cantina-susds-2024-09
  type: audit_report
  title: Cantina MakerDAO sUSDS Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/sdai/susds/audit/20240926-cantina-report-maker-susds.pdf
  path: audit-reports/cantina-susds-2024-09.pdf
  date_published: '2024-09-26'
  date_checked: '2026-06-08'
  content_sha256: 4123483f54e43db5287638ce033bba9366310c207f8f38219576484526a17b54
```

## Notes

`SUsds (L2)` has no selected active contracts-list row for `src/l2/SUsds.sol`.
