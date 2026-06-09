# ds-pause

## Codebases

```yaml
repositories:
- id: ds-pause
  name: ds-pause
  provider: github
  url: https://github.com/sky-ecosystem/ds-pause
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/ds-pause/branch-master"
    checked_out_branch: master
    pinned_commit: 5e798dd96bfaac978cd9fe3c0259b486e8afd213
- id: ds-pause-commit-81fd-ce3
  name: ds-pause
  provider: github
  url: https://github.com/sky-ecosystem/ds-pause
  ref: 81fd9d43e56615267a10e29710716342bcca0ce3
  ref_type: commit
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/ds-pause/commit-81fd-ce3"
    checked_out_branch: HEAD
    pinned_commit: 81fd9d43e56615267a10e29710716342bcca0ce3
```

## Deployments

```yaml
deployments:
- id: ds-pause-ethereum
  contract_id: ds-pause
  contract_name: DSPause
  status: live
  chain: Ethereum
  address: '0xbE286431454714F511008713973d3B053A2d38f3'
  implementation:
    codebase: ds-pause
    submodule_path: "./codebases/ds-pause/branch-master"
    source_path: src/pause.sol
    contract_name: DSPause
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
- id: ds-pause-proxy-ethereum
  contract_id: ds-pause-proxy
  contract_name: DSPauseProxy
  status: live
  chain: Ethereum
  address: '0xBE8E3e3618f7474F8cB1d074A26afFef007E98FB'
  implementation:
    codebase: ds-pause
    submodule_path: "./codebases/ds-pause/branch-master"
    source_path: src/pause.sol
    contract_name: DSPauseProxy
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
```

## Audit Reports

```yaml
audit_reports:
- id: trail-of-bits-mcd
  auditor: Trail of Bits
  report_title: MakerDAO Multi-Collateral Dai Final Report
  current_version: final
  versions:
  - id: final
    reference_refs:
    - trail-of-bits-mcd-final
    version_label: Final
    status: current
    audited_codebases:
    - ds-pause-commit-81fd-ce3
    audited_sources:
    - codebase: ds-pause-commit-81fd-ce3
      path: src/pause.sol
    covered_contracts:
    - id: ds-pause
      name: DSPause
    - id: ds-pause-proxy
      name: DSPauseProxy
    scope_notes: Trail of Bits MCD launch audit coverage lists ds-pause commit 81fd9d43e56615267a10e29710716342bcca0ce3 and names DSPause and DSPauseProxy.
references:
- id: trail-of-bits-mcd-final
  type: audit_report
  title: Trail of Bits MakerDAO Multi-Collateral Dai Final Report
  url: https://raw.githubusercontent.com/sky-ecosystem/mcd-security/master/Audit%20Reports/TOB_MakerDAO_Final_Report.pdf
  path: audit-reports/trail-of-bits-mcd-final.pdf
  date_checked: '2026-06-08'
  content_sha256: c8bbd2a107626ec96d4f61c663beb9be85c86eadc85c82debcefc2a7f0dfa458
  notes: Same report is also mapped to core-system/dss for MCD launch scope.
```
