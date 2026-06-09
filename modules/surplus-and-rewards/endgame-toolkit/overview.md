# endgame-toolkit

## Codebases

```yaml
repositories:
- id: endgame-toolkit
  name: endgame-toolkit
  provider: github
  url: https://github.com/sky-ecosystem/endgame-toolkit
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/endgame-toolkit/branch-master"
    checked_out_branch: master
    pinned_commit: db3cc6a4cc4852f3677055b7a37dbd0492ce2f9c
- id: endgame-toolkit-commit-70b5-a95
  name: endgame-toolkit
  provider: github
  url: https://github.com/sky-ecosystem/endgame-toolkit
  ref: 70b59deb7201758fcb7b81497a09c30b8aacda95
  ref_type: commit
  source_code_roots:
  - script
  - src
  checkout:
    submodule_path: "./codebases/endgame-toolkit/commit-70b5-a95"
    checked_out_branch: HEAD
    pinned_commit: 70b59deb7201758fcb7b81497a09c30b8aacda95
```

## Deployments

```yaml
deployments:
- id: sub-proxy-ethereum
  contract_id: sub-proxy
  contract_name: SubProxy
  status: live
  chain: Ethereum
  address: '0x3300f198988e4C9C63F75dF86De36421f06af8c4'
  implementation:
    codebase: endgame-toolkit
    submodule_path: "./codebases/endgame-toolkit/branch-master"
    source_path: src/SubProxy.sol
    contract_name: SubProxy
    compiler:
      version: 0.8.19
      optimized: false
      evm_version: default
- id: sdao-ethereum
  contract_id: sdao
  contract_name: SDAO
  status: live
  chain: Ethereum
  address: '0xc20059e0317DE91738d13af027DfC4a50781b066'
  implementation:
    codebase: endgame-toolkit
    submodule_path: "./codebases/endgame-toolkit/branch-master"
    source_path: src/SDAO.sol
    contract_name: SDAO
    compiler:
      version: 0.8.16
      optimized: true
      runs: 200
      evm_version: london
- id: vested-rewards-distribution-ethereum
  contract_id: vested-rewards-distribution
  contract_name: VestedRewardsDistribution
  status: live
  chain: Ethereum
  address: '0xC8d67Fcf101d3f89D0e1F3a2857485A84072a63F'
  implementation:
    codebase: endgame-toolkit
    submodule_path: "./codebases/endgame-toolkit/branch-master"
    source_path: src/VestedRewardsDistribution.sol
    contract_name: VestedRewardsDistribution
    compiler:
      version: 0.8.16
      optimized: true
      runs: 200
      evm_version: london
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-endgame-toolkit
  auditor: ChainSecurity
  report_title: Sky Endgame Toolkit Audit
  current_version: v2026-01
  versions:
  - id: v2026-01
    reference_refs:
    - chainsecurity-endgame-toolkit-2026-01
    version_label: January 2026
    status: current
    audited_codebases:
    - endgame-toolkit
    audited_sources:
    - codebase: endgame-toolkit
      path: src/SubProxy.sol
    - codebase: endgame-toolkit
      path: src/SDAO.sol
    - codebase: endgame-toolkit
      path: src/VestedRewardsDistribution.sol
    covered_contracts:
    - id: sub-proxy
      name: SubProxy
    - id: sdao
      name: SDAO
    - id: vested-rewards-distribution
      name: VestedRewardsDistribution
- id: cantina-endgame-toolkit
  auditor: Cantina
  report_title: Sky Endgame Toolkit Audit
  current_version: v2026-01
  versions:
  - id: v2026-01
    reference_refs:
    - cantina-endgame-toolkit-2026-01
    version_label: January 2026
    status: current
    audited_codebases:
    - endgame-toolkit
    audited_sources:
    - codebase: endgame-toolkit
      path: src/SubProxy.sol
    - codebase: endgame-toolkit
      path: src/SDAO.sol
    - codebase: endgame-toolkit
      path: src/VestedRewardsDistribution.sol
    covered_contracts:
    - id: sub-proxy
      name: SubProxy
    - id: sdao
      name: SDAO
    - id: vested-rewards-distribution
      name: VestedRewardsDistribution
- id: sherlock-endgame-toolkit
  auditor: Sherlock
  report_title: MakerDAO Endgame Audit Report
  current_version: final
  versions:
  - id: final
    reference_refs:
    - sherlock-endgame-toolkit-2024-08
    version_label: Final
    status: current
    audited_codebases:
    - endgame-toolkit-commit-70b5-a95
    audited_sources:
    - codebase: endgame-toolkit-commit-70b5-a95
      path: src/SubProxy.sol
    - codebase: endgame-toolkit-commit-70b5-a95
      path: src/SDAO.sol
    - codebase: endgame-toolkit-commit-70b5-a95
      path: src/VestedRewardsDistribution.sol
    covered_contracts:
    - id: sub-proxy
      name: SubProxy
    - id: sdao
      name: SDAO
    - id: vested-rewards-distribution
      name: VestedRewardsDistribution
    scope_notes: Sherlock public contest scope also included endgame-toolkit deployment scripts and synthetix staking rewards support files.
references:
- id: chainsecurity-endgame-toolkit-2026-01
  type: audit_report
  title: ChainSecurity Sky Endgame Toolkit Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/endgame-toolkit/master/audits/ChainSecurity_Sky_EndgameToolkit_Audit_v14_2026-01-13.pdf
  path: audit-reports/chainsecurity-endgame-toolkit-2026-01.pdf
  date_published: '2026-01-13'
  date_checked: '2026-06-08'
  content_sha256: 04ebb2ba50eda7608c34328b6405739f54c947a4156ba6440bf1a8c4dd82c701
- id: cantina-endgame-toolkit-2026-01
  type: audit_report
  title: Cantina Sky Endgame Toolkit Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/endgame-toolkit/master/audits/cantina_sky_endgame-toolkit_jan_2026-01-29.pdf
  path: audit-reports/cantina-endgame-toolkit-2026-01.pdf
  date_published: '2026-01-29'
  date_checked: '2026-06-08'
  content_sha256: 1b4a6d56bb0b36b0369ba86df7d50d4fead8188c36355c78a046826857464d4b
- id: sherlock-endgame-toolkit-2024-08
  type: audit_report
  title: Sherlock MakerDAO Endgame Audit Report
  url: https://raw.githubusercontent.com/sherlock-protocol/sherlock-reports/main/audits/2024.08.05%20-%20Final%20-%20MakerDAO%20Endgame%20Audit%20Report.pdf
  path: audit-reports/sherlock-endgame-toolkit-2024-08.pdf
  date_published: '2024-08-05'
  date_checked: '2026-06-08'
  content_sha256: 80b8fcebcdb454528209c9b78d40425ac0d97dc9e56cb08e176102b6f2ad6bfc
  notes: Public audit contest report listed by Sky security docs.
```

## Notes

`SDAO` is absent from the active contracts-list rows. The `VestedRewardsDistribution` address in `info.yaml` is disabled in the contracts list, so the contracts-list crosswalk selects active distribution rows with the same source.
