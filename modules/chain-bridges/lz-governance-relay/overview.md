# lz-governance-relay

## Codebases

```yaml
repositories:
- id: lz-governance-relay
  name: lz-governance-relay
  provider: github
  url: https://github.com/sky-ecosystem/lz-governance-relay
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: ff964bb030fd84f6f0d9718aa585fc90fdc9989e
- id: lz-governance-relay-commit-d3e3-d4ef
  name: lz-governance-relay
  provider: github
  url: https://github.com/sky-ecosystem/lz-governance-relay
  ref: d3e3df4db417f196fdd56123e7dbb462d04f32ef
  ref_type: commit
  source_code_roots:
  - src
  checkout:
    submodule_path: "./commit-d3e3-d4ef"
    checked_out_branch: HEAD
    pinned_commit: d3e3df4db417f196fdd56123e7dbb462d04f32ef
```

## Deployments

```yaml
deployments:
- id: l1-governance-relay-ethereum
  contract_id: l1-governance-relay
  contract_name: L1GovernanceRelay
  status: live
  chain: Ethereum
  address: '0x2beBFe397D497b66cB14461cB6ee467b4C3B7D61'
  implementation:
    codebase: lz-governance-relay
    submodule_path: "./branch-master"
    source_path: src/L1GovernanceRelay.sol
    contract_name: L1GovernanceRelay
    compiler:
      version: 0.8.22
      optimized: true
      runs: 200
      evm_version: shanghai
- id: l2-governance-relay-avalanche
  contract_id: l2-governance-relay
  contract_name: L2GovernanceRelay
  status: live
  chain: Avalanche
  address: '0xe928885BCe799Ed933651715608155F01abA23cA'
  implementation:
    codebase: lz-governance-relay
    submodule_path: "./branch-master"
    source_path: src/L2GovernanceRelay.sol
    contract_name: L2GovernanceRelay
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-sky-lz-governance-relay
  auditor: ChainSecurity
  report_title: Sky LZ Governance Relay Audit
  current_version: v2025-10
  versions:
  - id: v2025-10
    reference_refs:
    - chainsecurity-sky-lz-governance-relay-2025-10
    version_label: October 2025
    status: current
    audited_codebases:
    - lz-governance-relay
    - lz-governance-relay-commit-d3e3-d4ef
    audited_sources:
    - codebase: lz-governance-relay
      path: src/L1GovernanceRelay.sol
    - codebase: lz-governance-relay-commit-d3e3-d4ef
      path: src/L2GovernanceRelay.sol
    covered_contracts:
    - id: l1-governance-relay
      name: L1GovernanceRelay
    - id: l2-governance-relay
      name: L2GovernanceRelay
- id: cantina-sky-lz-gov-relay
  auditor: Cantina
  report_title: Sky LZ Governance Relay Audit
  current_version: v2025-09
  versions:
  - id: v2025-09
    reference_refs:
    - cantina-sky-lz-gov-relay-2025-09
    version_label: September 2025
    status: current
    audited_codebases:
    - lz-governance-relay
    - lz-governance-relay-commit-d3e3-d4ef
    audited_sources:
    - codebase: lz-governance-relay
      path: src/L1GovernanceRelay.sol
    - codebase: lz-governance-relay-commit-d3e3-d4ef
      path: src/L2GovernanceRelay.sol
    covered_contracts:
    - id: l1-governance-relay
      name: L1GovernanceRelay
    - id: l2-governance-relay
      name: L2GovernanceRelay
references:
- id: chainsecurity-sky-lz-governance-relay-2025-10
  type: audit_report
  title: ChainSecurity Sky LZ Governance Relay Audit
  url: https://reports.chainsecurity.com/Sky/ChainSecurity_Sky_SkyLZGovernanceRelay_Audit.pdf
  path: audit-reports/chainsecurity-sky-lz-governance-relay-2025-10.pdf
  date_published: 2025-10
  date_checked: '2026-06-08'
  content_sha256: 23a24bb6d900288c2f0229b4b07c068599e4e0f2185e34df3a57968b446c092e
- id: cantina-sky-lz-gov-relay-2025-09
  type: audit_report
  title: Cantina Sky LZ Governance Relay Audit
  url: https://cdn.cantina.xyz/reports/cantina_sky_lz_gov_relay_sep2025.pdf
  path: audit-reports/cantina-sky-lz-gov-relay-2025-09.pdf
  date_published: 2025-09
  date_checked: '2026-06-08'
  content_sha256: e1555ac7064192b330c8f8bebb0b314551d8e86df2aa9d40c9764016bf4a61e3
```
