# usds

## Codebases

```yaml
repositories:
- id: usds
  name: usds
  provider: github
  url: https://github.com/sky-ecosystem/usds
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/usds/branch-master"
    checked_out_branch: master
    pinned_commit: d65551dbc11cfe1afcc4718ab790663b99d766af
```

## Deployments

```yaml
deployments:
- id: usds-ethereum
  contract_id: usds
  contract_name: Usds
  status: live
  chain: Ethereum
  address: '0x1923DfeE706A8E78157416C29cBCCFDe7cdF4102'
  implementation:
    codebase: usds
    submodule_path: "./codebases/usds/branch-master"
    source_path: src/Usds.sol
    contract_name: Usds
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
- id: usds-join-ethereum
  contract_id: usds-join
  contract_name: UsdsJoin
  status: live
  chain: Ethereum
  address: '0x3C0f895007CA717Aa01c8693e59DF1e8C3777FEB'
  implementation:
    codebase: usds
    submodule_path: "./codebases/usds/branch-master"
    source_path: src/UsdsJoin.sol
    contract_name: UsdsJoin
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
- id: dai-usds-ethereum
  contract_id: dai-usds
  contract_name: DaiUsds
  status: live
  chain: Ethereum
  address: '0x3225737a9Bbb6473CB4a45b7244ACa2BeFdB276A'
  implementation:
    codebase: usds
    submodule_path: "./codebases/usds/branch-master"
    source_path: src/DaiUsds.sol
    contract_name: DaiUsds
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-usds
  auditor: ChainSecurity
  report_title: MakerDAO USDS Audit
  current_version: v2024-09
  versions:
  - id: v2024-09
    reference_refs:
    - chainsecurity-usds-2024-09
    version_label: September 2024
    status: current
    audited_codebases:
    - usds
    audited_sources:
    - codebase: usds
      path: src/Usds.sol
    - codebase: usds
      path: src/UsdsJoin.sol
    - codebase: usds
      path: src/DaiUsds.sol
    covered_contracts:
    - id: usds
      name: Usds
    - id: usds-join
      name: UsdsJoin
    - id: dai-usds
      name: DaiUsds
- id: cantina-usds
  auditor: Cantina
  report_title: MakerDAO USDS Audit
  current_version: v2024-09
  versions:
  - id: v2024-09
    reference_refs:
    - cantina-usds-2024-09
    version_label: September 2024
    status: current
    audited_codebases:
    - usds
    audited_sources:
    - codebase: usds
      path: src/Usds.sol
    - codebase: usds
      path: src/UsdsJoin.sol
    - codebase: usds
      path: src/DaiUsds.sol
    covered_contracts:
    - id: usds
      name: Usds
    - id: usds-join
      name: UsdsJoin
    - id: dai-usds
      name: DaiUsds
references:
- id: chainsecurity-usds-2024-09
  type: audit_report
  title: ChainSecurity MakerDAO USDS Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/usds/master/audit/20240930-ChainSecurity_MakerDAO_USDS_audit.pdf
  path: audit-reports/chainsecurity-usds-2024-09.pdf
  date_published: '2024-09-30'
  date_checked: '2026-06-08'
  content_sha256: a54c56931380f4931b52a7d7d79794e9879f5e43540bd02afa8364b299311c82
- id: cantina-usds-2024-09
  type: audit_report
  title: Cantina MakerDAO USDS Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/usds/master/audit/20240926-cantina-report-review-makerdao-usds.pdf
  path: audit-reports/cantina-usds-2024-09.pdf
  date_published: '2024-09-26'
  date_checked: '2026-06-08'
  content_sha256: 4231acb9bb5ae4c26373df39ddc25cde03be8f109983ec7e756df80ff240741a
```
