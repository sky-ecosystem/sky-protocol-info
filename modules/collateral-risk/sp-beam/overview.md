# sp-beam

## Codebases

```yaml
repositories:
- id: sp-beam
  name: sp-beam
  provider: github
  url: https://github.com/sky-ecosystem/sp-beam
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: bc8857955fa0245b015d45ec661ab4757925db44
```

## Deployments

```yaml
deployments:
- id: spbeam-ethereum
  contract_id: spbeam
  contract_name: SPBEAM
  status: live
  chain: Ethereum
  address: '0x36B072ed8AFE665E3Aa6DaBa79Decbec63752b22'
  implementation:
    codebase: sp-beam
    submodule_path: "./branch-master"
    source_path: src/SPBEAM.sol
    contract_name: SPBEAM
    compiler:
      version: 0.8.24
      optimized: true
      runs: 200
      evm_version: cancun
- id: spbeam-mom-ethereum
  contract_id: spbeam-mom
  contract_name: SPBEAMMom
  status: live
  chain: Ethereum
  address: '0xf0C6e6Ec8B367cC483A411e595D3Ba0a816d37D0'
  implementation:
    codebase: sp-beam
    submodule_path: "./branch-master"
    source_path: src/SPBEAMMom.sol
    contract_name: SPBEAMMom
    compiler:
      version: 0.8.24
      optimized: true
      runs: 200
      evm_version: cancun
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-sp-beam
  auditor: ChainSecurity
  report_title: Sky SP-BEAM Module Audit
  current_version: v1
  versions:
  - id: v1
    reference_refs:
    - chainsecurity-sp-beam
    status: current
    audited_codebases:
    - sp-beam
    audited_sources:
    - codebase: sp-beam
      path: src/SPBEAM.sol
    - codebase: sp-beam
      path: src/SPBEAMMom.sol
    covered_contracts:
    - id: spbeam
      name: SPBEAM
    - id: spbeam-mom
      name: SPBEAMMom
- id: cantina-sp-beam
  auditor: Cantina
  report_title: Maker SP-BEAM Audit
  current_version: v2025-03
  versions:
  - id: v2025-03
    reference_refs:
    - cantina-sp-beam-2025-03
    version_label: March 2025
    status: current
    audited_codebases:
    - sp-beam
    audited_sources:
    - codebase: sp-beam
      path: src/SPBEAM.sol
    - codebase: sp-beam
      path: src/SPBEAMMom.sol
    covered_contracts:
    - id: spbeam
      name: SPBEAM
    - id: spbeam-mom
      name: SPBEAMMom
references:
- id: chainsecurity-sp-beam
  type: audit_report
  title: ChainSecurity Sky SP-BEAM Module Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/sp-beam/master/audits/ChainSecurity_Sky_SP-BEAM_Module_audit.pdf
  path: audit-reports/chainsecurity-sp-beam.pdf
  date_checked: '2026-06-08'
  content_sha256: 1e60cbdaff8f1a5aa7ad6097bbdcedd4da4380eca3b5f119d78f3de15d849872
- id: cantina-sp-beam-2025-03
  type: audit_report
  title: Cantina Maker SP-BEAM Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/sp-beam/master/audits/cantina_maker_sp_beam_march2025.pdf
  path: audit-reports/cantina-sp-beam-2025-03.pdf
  date_published: 2025-03
  date_checked: '2026-06-08'
  content_sha256: 6f8a407f1e29510e36ea2a6941967c137a697cdb84d349101d3fb6d65881b097
```
