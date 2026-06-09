# star-guard

## Codebases

```yaml
repositories:
- id: star-guard
  name: star-guard
  provider: github
  url: https://github.com/sky-ecosystem/star-guard
  ref: main
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-main"
    checked_out_branch: main
    pinned_commit: 52239d716a89188b303f137fc43fb9288735ba2e
```

## Deployments

```yaml
deployments:
- id: star-guard-ethereum
  contract_id: star-guard
  contract_name: StarGuard
  status: live
  chain: Ethereum
  address: '0x6605aa120fe8b656482903E7757BaBF56947E45E'
  implementation:
    codebase: star-guard
    submodule_path: "./branch-main"
    source_path: src/StarGuard.sol
    contract_name: StarGuard
    compiler:
      version: 0.8.24
      optimized: false
      evm_version: cancun
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-star-guard
  auditor: ChainSecurity
  report_title: Sky StarGuard Audit
  current_version: v2025-10
  versions:
  - id: v2025-10
    reference_refs:
    - chainsecurity-star-guard-2025-10
    version_label: October 2025
    status: current
    audited_codebases:
    - star-guard
    audited_sources:
    - codebase: star-guard
      path: src/StarGuard.sol
    covered_contracts:
    - id: star-guard
      name: StarGuard
- id: cantina-star-guard
  auditor: Cantina
  report_title: Sky Star Guard Audit
  current_version: v2025-10
  versions:
  - id: v2025-10
    reference_refs:
    - cantina-star-guard-2025-10
    version_label: October 2025
    status: current
    audited_codebases:
    - star-guard
    audited_sources:
    - codebase: star-guard
      path: src/StarGuard.sol
    covered_contracts:
    - id: star-guard
      name: StarGuard
references:
- id: chainsecurity-star-guard-2025-10
  type: audit_report
  title: ChainSecurity Sky StarGuard Audit
  url: https://reports.chainsecurity.com/Sky/ChainSecurity_Sky_StarGuard_Audit.pdf
  path: audit-reports/chainsecurity-star-guard-2025-10.pdf
  date_published: 2025-10
  date_checked: '2026-06-08'
  content_sha256: 1f27b91fe89cbe63ecaf9d1f5e82d4b0e4e07f266f5a7833021014cfd997da6a
- id: cantina-star-guard-2025-10
  type: audit_report
  title: Cantina Sky Star Guard Audit
  url: https://cdn.cantina.xyz/reports/cantina_sky_star_guard_oct2025.pdf
  path: audit-reports/cantina-star-guard-2025-10.pdf
  date_published: 2025-10
  date_checked: '2026-06-08'
  content_sha256: 3dae62bd2547b958cc2e5e46de9cd6d1a047f9aedabc23c709ff005d21b0ebe8
```
