# lockstake

## Codebases

```yaml
repositories:
- id: lockstake
  name: lockstake
  provider: github
  url: https://github.com/sky-ecosystem/lockstake
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: e389dc18fa21b5ae460714522a9f484d0b1b9f30
```

## Deployments

```yaml
deployments:
- id: lockstake-engine-ethereum
  contract_id: lockstake-engine
  contract_name: LockstakeEngine
  status: live
  chain: Ethereum
  address: '0xCe01C90dE7FD1bcFa39e237FE6D8D9F569e8A6a3'
  implementation:
    codebase: lockstake
    submodule_path: "./branch-master"
    source_path: src/LockstakeEngine.sol
    contract_name: LockstakeEngine
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
- id: lockstake-clipper-ethereum
  contract_id: lockstake-clipper
  contract_name: LockstakeClipper
  status: live
  chain: Ethereum
  address: '0x836F56750517b1528B5078Cba4Ac4B94fBE4A399'
  implementation:
    codebase: lockstake
    submodule_path: "./branch-master"
    source_path: src/LockstakeClipper.sol
    contract_name: LockstakeClipper
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
- id: lockstake-sky-ethereum
  contract_id: lockstake-sky
  contract_name: LockstakeSky
  status: live
  chain: Ethereum
  address: '0xf9A9cfD3229E985B91F99Bc866d42938044FFa1C'
  implementation:
    codebase: lockstake
    submodule_path: "./branch-master"
    source_path: src/LockstakeSky.sol
    contract_name: LockstakeSky
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
- id: lockstake-capped-osm-wrapper-ethereum
  contract_id: lockstake-capped-osm-wrapper
  contract_name: LockstakeCappedOsmWrapper
  status: live
  chain: Ethereum
  address: '0x0C13fF3DC02E85aC169c4099C09c9B388f2943Fd'
  implementation:
    codebase: lockstake
    submodule_path: "./branch-master"
    source_path: src/LockstakeCappedOsmWrapper.sol
    contract_name: LockstakeCappedOsmWrapper
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
deployment_gaps:
- contract_id: lockstake-urn
  contract_name: LockstakeUrn
  implementation:
    codebase: lockstake
    submodule_path: "./branch-master"
    source_path: src/LockstakeUrn.sol
    contract_name: LockstakeUrn
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-lockstake
  auditor: ChainSecurity
  report_title: Sky Lockstake Audit
  current_version: v2025-09
  versions:
  - id: v2025-09
    reference_refs:
    - chainsecurity-lockstake-2025-09
    version_label: September 2025
    status: current
    audited_codebases:
    - lockstake
    audited_sources:
    - codebase: lockstake
      path: src/LockstakeEngine.sol
    - codebase: lockstake
      path: src/LockstakeClipper.sol
    - codebase: lockstake
      path: src/LockstakeSky.sol
    - codebase: lockstake
      path: src/LockstakeUrn.sol
    - codebase: lockstake
      path: src/LockstakeCappedOsmWrapper.sol
    covered_contracts:
    - id: lockstake-engine
      name: LockstakeEngine
    - id: lockstake-clipper
      name: LockstakeClipper
    - id: lockstake-sky
      name: LockstakeSky
    - id: lockstake-urn
      name: LockstakeUrn
    - id: lockstake-capped-osm-wrapper
      name: LockstakeCappedOsmWrapper
- id: cantina-lockstake
  auditor: Cantina
  report_title: Sky Lockstake Audit
  current_version: v2025-09
  versions:
  - id: v2025-09
    reference_refs:
    - cantina-lockstake-2025-09
    version_label: September 2025
    status: current
    audited_codebases:
    - lockstake
    audited_sources:
    - codebase: lockstake
      path: src/LockstakeEngine.sol
    - codebase: lockstake
      path: src/LockstakeClipper.sol
    - codebase: lockstake
      path: src/LockstakeSky.sol
    - codebase: lockstake
      path: src/LockstakeUrn.sol
    - codebase: lockstake
      path: src/LockstakeCappedOsmWrapper.sol
    covered_contracts:
    - id: lockstake-engine
      name: LockstakeEngine
    - id: lockstake-clipper
      name: LockstakeClipper
    - id: lockstake-sky
      name: LockstakeSky
    - id: lockstake-urn
      name: LockstakeUrn
    - id: lockstake-capped-osm-wrapper
      name: LockstakeCappedOsmWrapper
references:
- id: chainsecurity-lockstake-2025-09
  type: audit_report
  title: ChainSecurity Sky Lockstake Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/lockstake/master/audit/20250926-ChainSecurity_Sky_Lockstake_audit.pdf
  path: audit-reports/chainsecurity-lockstake-2025-09.pdf
  date_published: '2025-09-26'
  date_checked: '2026-06-08'
  content_sha256: 44fa8093ac0c422dffb49f28a59714d3e484c5f166e55c21235384ccf406855a
- id: cantina-lockstake-2025-09
  type: audit_report
  title: Cantina Sky Lockstake Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/lockstake/master/audit/20250929-cantina-report-sky-lockstake.pdf
  path: audit-reports/cantina-lockstake-2025-09.pdf
  date_published: '2025-09-29'
  date_checked: '2026-06-08'
  content_sha256: e37a5e1e71c8c132ba81bf629a8fe79189e46a1e4e9f17dead28b0df9815862e
```

## Notes

`LockstakeUrn` has no deployed address in `info.yaml` and no selected active contracts-list row.
