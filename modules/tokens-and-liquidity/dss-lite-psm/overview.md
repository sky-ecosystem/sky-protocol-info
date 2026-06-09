# dss-lite-psm

## Codebases

```yaml
repositories:
- id: dss-lite-psm
  name: dss-lite-psm
  provider: github
  url: https://github.com/sky-ecosystem/dss-lite-psm
  ref: main
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-main"
    checked_out_branch: main
    pinned_commit: dbf0022225f645f5697e5517d0cf00810471bccf
```

## Deployments

```yaml
deployments:
- id: dss-lite-psm-ethereum
  contract_id: dss-lite-psm
  contract_name: DssLitePsm
  status: live
  chain: Ethereum
  address: '0xf6e72Db5454dd049d0788e411b06CfAF16853042'
  implementation:
    codebase: dss-lite-psm
    submodule_path: "./branch-main"
    source_path: src/DssLitePsm.sol
    contract_name: DssLitePsm
    compiler:
      version: 0.8.16
      optimized: true
      runs: 200
      evm_version: london
- id: dss-lite-psm-mom-ethereum
  contract_id: dss-lite-psm-mom
  contract_name: DssLitePsmMom
  status: live
  chain: Ethereum
  address: '0x467b32b0407Ad764f56304420Cddaa563bDab425'
  implementation:
    codebase: dss-lite-psm
    submodule_path: "./branch-main"
    source_path: src/DssLitePsmMom.sol
    contract_name: DssLitePsmMom
    compiler:
      version: 0.8.16
      optimized: true
      runs: 200
      evm_version: london
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-dss-lite-psm
  auditor: ChainSecurity
  report_title: MakerDAO PSM Lite Audit
  current_version: v1
  versions:
  - id: v1
    reference_refs:
    - chainsecurity-dss-lite-psm
    status: current
    audited_codebases:
    - dss-lite-psm
    audited_sources:
    - codebase: dss-lite-psm
      path: src/DssLitePsm.sol
    - codebase: dss-lite-psm
      path: src/DssLitePsmMom.sol
    covered_contracts:
    - id: dss-lite-psm
      name: DssLitePsm
    - id: dss-lite-psm-mom
      name: DssLitePsmMom
- id: cantina-dss-lite-psm
  auditor: Cantina
  report_title: MakerDAO DSS Lite PSM Audit
  current_version: v1
  versions:
  - id: v1
    reference_refs:
    - cantina-dss-lite-psm
    status: current
    audited_codebases:
    - dss-lite-psm
    audited_sources:
    - codebase: dss-lite-psm
      path: src/DssLitePsm.sol
    - codebase: dss-lite-psm
      path: src/DssLitePsmMom.sol
    covered_contracts:
    - id: dss-lite-psm
      name: DssLitePsm
    - id: dss-lite-psm-mom
      name: DssLitePsmMom
references:
- id: chainsecurity-dss-lite-psm
  type: audit_report
  title: ChainSecurity MakerDAO PSM Lite Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-lite-psm/main/audits/ChainSecurity_MakerDAO_PSM_Lite_audit.pdf
  path: audit-reports/chainsecurity-dss-lite-psm.pdf
  date_checked: '2026-06-08'
  content_sha256: a9734120dd00ddd9db10ad5092fd67bfa1e000f8a7626610f2b75bdf813b7a3b
- id: cantina-dss-lite-psm
  type: audit_report
  title: Cantina MakerDAO DSS Lite PSM Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-lite-psm/main/audits/report-review-makerdao-dss-lite-psm.pdf
  path: audit-reports/cantina-dss-lite-psm.pdf
  date_checked: '2026-06-08'
  content_sha256: 3eea05313c5df928b84b2821010aea671a2839467a790aba8c7f72e598c201ee
```
