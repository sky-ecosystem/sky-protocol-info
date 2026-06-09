# dss-vest

## Codebases

```yaml
repositories:
- id: dss-vest
  name: dss-vest
  provider: github
  url: https://github.com/sky-ecosystem/dss-vest
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: e9e6a779fc0ab8b05711fba190765f50bb1d77a2
```

## Deployments

```yaml
deployments:
- id: dss-vest-transferrable-ethereum
  contract_id: dss-vest-transferrable
  contract_name: DssVestTransferrable
  status: live
  chain: Ethereum
  address: '0x67eaDb3288cceDe034cE95b0511DCc65cf630bB6'
  implementation:
    codebase: dss-vest
    submodule_path: "./branch-master"
    source_path: src/DssVest.sol
    contract_name: DssVestTransferrable
    compiler:
      version: 0.6.12
      optimized: true
      runs: 200
      evm_version: istanbul
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-dss-vest
  auditor: ChainSecurity
  report_title: MakerDAO DSS Vest Audit
  current_version: v1
  versions:
  - id: v1
    reference_refs:
    - chainsecurity-dss-vest
    status: current
    audited_codebases:
    - dss-vest
    audited_sources:
    - codebase: dss-vest
      path: src/DssVest.sol
    covered_contracts:
    - id: dss-vest-transferrable
      name: DssVestTransferrable
- id: abdk-dss-vest
  auditor: ABDK
  report_title: DSS Vest Audit
  current_version: audit5a
  versions:
  - id: audit5a
    reference_refs:
    - abdk-dss-vest
    version_label: Audit5a
    status: current
    audited_codebases:
    - dss-vest
    audited_sources:
    - codebase: dss-vest
      path: src/DssVest.sol
    covered_contracts:
    - id: dss-vest-transferrable
      name: DssVestTransferrable
references:
- id: chainsecurity-dss-vest
  type: audit_report
  title: ChainSecurity MakerDAO DSS Vest Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-vest/master/audits/ChainSecurity_MakerDAO_DSS_Vest_audit.pdf
  path: audit-reports/chainsecurity-dss-vest.pdf
  date_checked: '2026-06-08'
  content_sha256: d5f44375274e90ac574ce028508f6f5dbc5473bdac8de218b2f5f87fab0f62be
- id: abdk-dss-vest
  type: audit_report
  title: ABDK DSS Vest Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-vest/master/audits/ABDK_DSSVest_Audit5a.pdf
  path: audit-reports/abdk-dss-vest.pdf
  date_checked: '2026-06-08'
  content_sha256: 99311867360ddb163768b7e3943d3657bbc6a3ca711046c0408319c9f8f4ba40
```
