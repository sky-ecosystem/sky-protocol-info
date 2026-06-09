# dss-allocator

## Codebases

```yaml
repositories:
- id: dss-allocator
  name: dss-allocator
  provider: github
  url: https://github.com/sky-ecosystem/dss-allocator
  ref: dev
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-dev"
    checked_out_branch: dev
    pinned_commit: 6e99d87374cff66e93fe44c55d4ed240dac1c3dc
```

## Deployments

```yaml
deployments:
- id: allocator-vault-ethereum
  contract_id: allocator-vault
  contract_name: AllocatorVault
  status: live
  chain: Ethereum
  address: '0x691a6c29e9e96dd897718305427Ad5D534db16BA'
  implementation:
    codebase: dss-allocator
    submodule_path: "./branch-dev"
    source_path: src/AllocatorVault.sol
    contract_name: AllocatorVault
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: london
- id: allocator-buffer-ethereum
  contract_id: allocator-buffer
  contract_name: AllocatorBuffer
  status: live
  chain: Ethereum
  address: '0xc395D150e71378B47A1b8E9de0c1a83b75a08324'
  implementation:
    codebase: dss-allocator
    submodule_path: "./branch-dev"
    source_path: src/AllocatorBuffer.sol
    contract_name: AllocatorBuffer
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: london
- id: allocator-registry-ethereum
  contract_id: allocator-registry
  contract_name: AllocatorRegistry
  status: live
  chain: Ethereum
  address: '0xCdCFA95343DA7821fdD01dc4d0AeDA958051bB3B'
  implementation:
    codebase: dss-allocator
    submodule_path: "./branch-dev"
    source_path: src/AllocatorRegistry.sol
    contract_name: AllocatorRegistry
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: london
- id: allocator-roles-ethereum
  contract_id: allocator-roles
  contract_name: AllocatorRoles
  status: live
  chain: Ethereum
  address: '0x9A865A710399cea85dbD9144b7a09C889e94E803'
  implementation:
    codebase: dss-allocator
    submodule_path: "./branch-dev"
    source_path: src/AllocatorRoles.sol
    contract_name: AllocatorRoles
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: london
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-dss-allocator
  auditor: ChainSecurity
  report_title: MakerDAO Allocator Audit
  current_version: v2024-09
  versions:
  - id: v2024-09
    reference_refs:
    - chainsecurity-dss-allocator-2024-09
    version_label: September 2024
    status: current
    audited_codebases:
    - dss-allocator
    audited_sources:
    - codebase: dss-allocator
      path: src/AllocatorBuffer.sol
    - codebase: dss-allocator
      path: src/AllocatorOracle.sol
    - codebase: dss-allocator
      path: src/AllocatorRegistry.sol
    - codebase: dss-allocator
      path: src/AllocatorRoles.sol
    - codebase: dss-allocator
      path: src/AllocatorVault.sol
    covered_contracts:
    - id: allocator-vault
      name: AllocatorVault
    - id: allocator-buffer
      name: AllocatorBuffer
    - id: allocator-registry
      name: AllocatorRegistry
    - id: allocator-roles
      name: AllocatorRoles
    - id: allocator-oracle
      name: AllocatorOracle
- id: chainsecurity-dss-allocator-deployment-scripts
  auditor: ChainSecurity
  report_title: MakerDAO Allocator Deployment Scripts Audit
  current_version: v2024-09
  versions:
  - id: v2024-09
    reference_refs:
    - chainsecurity-dss-allocator-deployment-scripts-2024-09
    version_label: September 2024
    status: current
    audited_codebases:
    - dss-allocator
    scope_notes: Deployment script audit from the module codebase audit folder.
- id: fps-dss-allocator
  auditor: FPS
  report_title: dss-allocator Assessment Final
  current_version: final
  versions:
  - id: final
    reference_refs:
    - fps-dss-allocator-final
    version_label: Final
    status: current
    audited_codebases:
    - dss-allocator
    audited_sources:
    - codebase: dss-allocator
      path: src/AllocatorBuffer.sol
    - codebase: dss-allocator
      path: src/AllocatorOracle.sol
    - codebase: dss-allocator
      path: src/AllocatorRegistry.sol
    - codebase: dss-allocator
      path: src/AllocatorRoles.sol
    - codebase: dss-allocator
      path: src/AllocatorVault.sol
    covered_contracts:
    - id: allocator-vault
      name: AllocatorVault
    - id: allocator-buffer
      name: AllocatorBuffer
    - id: allocator-registry
      name: AllocatorRegistry
    - id: allocator-roles
      name: AllocatorRoles
    - id: allocator-oracle
      name: AllocatorOracle
- id: cantina-dss-allocator
  auditor: Cantina
  report_title: MakerDAO DSS Allocator Audit
  current_version: v1
  versions:
  - id: v1
    reference_refs:
    - cantina-dss-allocator
    status: current
    audited_codebases:
    - dss-allocator
    audited_sources:
    - codebase: dss-allocator
      path: src/AllocatorBuffer.sol
    - codebase: dss-allocator
      path: src/AllocatorOracle.sol
    - codebase: dss-allocator
      path: src/AllocatorRegistry.sol
    - codebase: dss-allocator
      path: src/AllocatorRoles.sol
    - codebase: dss-allocator
      path: src/AllocatorVault.sol
    covered_contracts:
    - id: allocator-vault
      name: AllocatorVault
    - id: allocator-buffer
      name: AllocatorBuffer
    - id: allocator-registry
      name: AllocatorRegistry
    - id: allocator-roles
      name: AllocatorRoles
    - id: allocator-oracle
      name: AllocatorOracle
references:
- id: chainsecurity-dss-allocator-2024-09
  type: audit_report
  title: ChainSecurity MakerDAO Allocator Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-allocator/dev/audit/20240909-ChainSecurity_MakerDAO_Allocator_audit.pdf
  path: audit-reports/chainsecurity-dss-allocator-2024-09.pdf
  date_published: '2024-09-09'
  date_checked: '2026-06-08'
  content_sha256: 771bdfc20cb0c1850ca80201c368f35b1d0828374245367d24a33860b2ad98ac
- id: chainsecurity-dss-allocator-deployment-scripts-2024-09
  type: audit_report
  title: ChainSecurity MakerDAO Allocator Deployment Scripts Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-allocator/dev/audit/20240909-ChainSecurity_MakerDAO_Allocator_Deployment_Scripts_audit.pdf
  path: audit-reports/chainsecurity-dss-allocator-deployment-scripts-2024-09.pdf
  date_published: '2024-09-09'
  date_checked: '2026-06-08'
  content_sha256: 583e69e2cc44cc7ddb23331ac79bbc8ed3b4dd63c0cb43661c73b7ccd07470ce
- id: fps-dss-allocator-final
  type: audit_report
  title: FPS dss-allocator Assessment Final
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-allocator/dev/audit/FPS_dss-allocator_Assessment_FINAL.pdf
  path: audit-reports/fps-dss-allocator-final.pdf
  date_checked: '2026-06-08'
  content_sha256: 505c19bd299acefcb24567a8625296680d8c39eca79e5e698b7ca61bc136fa76
- id: cantina-dss-allocator
  type: audit_report
  title: Cantina MakerDAO DSS Allocator Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-allocator/dev/audit/cantina-report-review-makerdao-dssallocator.pdf
  path: audit-reports/cantina-dss-allocator.pdf
  date_checked: '2026-06-08'
  content_sha256: 3502eef86fbb9a1d4079ab16301487588c0198920c603ee6596c73d5ac23a23f
```

## Notes

`AllocatorOracle` has a contract/source record but no live deployment record in the source metadata.
