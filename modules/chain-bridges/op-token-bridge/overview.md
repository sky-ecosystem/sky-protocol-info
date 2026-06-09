# op-token-bridge

## Codebases

```yaml
repositories:
- id: op-token-bridge
  name: op-token-bridge
  provider: github
  url: https://github.com/sky-ecosystem/op-token-bridge
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: 82918f4853d50c6520dac53fdb70a42fd4ce671b
```

## Deployments

```yaml
deployments:
- id: l1-governance-relay-ethereum
  contract_id: l1-governance-relay
  contract_name: L1GovernanceRelay
  status: live
  chain: Ethereum
  address: '0x1Ee0AE8A993F2f5abDB51EAF4AC2876202b65c3b'
  implementation:
    codebase: op-token-bridge
    submodule_path: "./branch-master"
    source_path: src/L1GovernanceRelay.sol
    contract_name: L1GovernanceRelay
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
- id: l2-governance-relay-base
  contract_id: l2-governance-relay
  contract_name: L2GovernanceRelay
  status: live
  chain: Base
  address: '0xdD0BCc201C9E47c6F6eE68E4dB05b652Bb6aC255'
  implementation:
    codebase: op-token-bridge
    submodule_path: "./branch-master"
    source_path: src/L2GovernanceRelay.sol
    contract_name: L2GovernanceRelay
- id: l1-token-bridge-ethereum
  contract_id: l1-token-bridge
  contract_name: L1TokenBridge
  status: live
  chain: Ethereum
  address: '0xaeFd31c2e593Dc971f9Cb42cBbD5d4AD7F1970b6'
  implementation:
    codebase: op-token-bridge
    submodule_path: "./branch-master"
    source_path: src/L1TokenBridge.sol
    contract_name: L1TokenBridge
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
- id: l2-token-bridge-base
  contract_id: l2-token-bridge
  contract_name: L2TokenBridge
  status: live
  chain: Base
  address: '0xee44cdb68D618d58F75d9fe0818B640BD7B8A7B7'
  implementation:
    codebase: op-token-bridge
    submodule_path: "./branch-master"
    source_path: src/L2TokenBridge.sol
    contract_name: L2TokenBridge
- id: escrow-ethereum
  contract_id: escrow
  contract_name: Escrow
  status: live
  chain: Ethereum
  address: '0x7F311a4D48377030bD810395f4CCfC03bdbe9Ef3'
  implementation:
    codebase: op-token-bridge
    submodule_path: "./branch-master"
    source_path: src/Escrow.sol
    contract_name: Escrow
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-op-token-bridge
  auditor: ChainSecurity
  report_title: MakerDAO OP Token Bridge Audit
  current_version: v2024-10
  versions:
  - id: v2024-10
    reference_refs:
    - chainsecurity-op-token-bridge-2024-10
    version_label: October 2024
    status: current
    audited_codebases:
    - op-token-bridge
    audited_sources:
    - codebase: op-token-bridge
      path: src/Escrow.sol
    - codebase: op-token-bridge
      path: src/L1GovernanceRelay.sol
    - codebase: op-token-bridge
      path: src/L1TokenBridge.sol
    - codebase: op-token-bridge
      path: src/L2GovernanceRelay.sol
    - codebase: op-token-bridge
      path: src/L2TokenBridge.sol
    covered_contracts:
    - id: escrow
      name: Escrow
    - id: l1-governance-relay
      name: L1GovernanceRelay
    - id: l1-token-bridge
      name: L1TokenBridge
    - id: l2-governance-relay
      name: L2GovernanceRelay
    - id: l2-token-bridge
      name: L2TokenBridge
- id: cantina-op-token-bridge
  auditor: Cantina
  report_title: MakerDAO OP Token Bridge Audit
  current_version: v2024-10
  versions:
  - id: v2024-09
    reference_refs:
    - cantina-op-token-bridge-2024-09
    version_label: September 2024
    status: superseded
    superseded_by: v2024-10
    audited_codebases:
    - op-token-bridge
    audited_sources:
    - codebase: op-token-bridge
      path: src/Escrow.sol
    - codebase: op-token-bridge
      path: src/L1GovernanceRelay.sol
    - codebase: op-token-bridge
      path: src/L1TokenBridge.sol
    - codebase: op-token-bridge
      path: src/L2GovernanceRelay.sol
    - codebase: op-token-bridge
      path: src/L2TokenBridge.sol
    covered_contracts:
    - id: escrow
      name: Escrow
    - id: l1-governance-relay
      name: L1GovernanceRelay
    - id: l1-token-bridge
      name: L1TokenBridge
    - id: l2-governance-relay
      name: L2GovernanceRelay
    - id: l2-token-bridge
      name: L2TokenBridge
  - id: v2024-10
    reference_refs:
    - cantina-op-token-bridge-2024-10
    version_label: October 2024
    status: current
    supersedes:
    - v2024-09
    audited_codebases:
    - op-token-bridge
    audited_sources:
    - codebase: op-token-bridge
      path: src/Escrow.sol
    - codebase: op-token-bridge
      path: src/L1GovernanceRelay.sol
    - codebase: op-token-bridge
      path: src/L1TokenBridge.sol
    - codebase: op-token-bridge
      path: src/L2GovernanceRelay.sol
    - codebase: op-token-bridge
      path: src/L2TokenBridge.sol
    covered_contracts:
    - id: escrow
      name: Escrow
    - id: l1-governance-relay
      name: L1GovernanceRelay
    - id: l1-token-bridge
      name: L1TokenBridge
    - id: l2-governance-relay
      name: L2GovernanceRelay
    - id: l2-token-bridge
      name: L2TokenBridge
references:
- id: chainsecurity-op-token-bridge-2024-10
  type: audit_report
  title: ChainSecurity MakerDAO OP Token Bridge Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/op-token-bridge/master/audit/20241009-ChainSecurity_MakerDAO_OP_Token_Bridge_audit.pdf
  path: audit-reports/chainsecurity-op-token-bridge-2024-10.pdf
  date_published: '2024-10-09'
  date_checked: '2026-06-08'
  content_sha256: d69a2d70c4362be6726f950b620d7fe831d103b96e8856b7aa55f1438a8c762c
- id: cantina-op-token-bridge-2024-09
  type: audit_report
  title: Cantina MakerDAO OP Token Bridge Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/op-token-bridge/master/audit/20240909-cantina-report-review-makerdao-op-token-bridge.pdf
  path: audit-reports/cantina-op-token-bridge-2024-09.pdf
  date_published: '2024-09-09'
  date_checked: '2026-06-08'
  content_sha256: 654ccf8e147dddfdccfc8df8ebb13e92bea4ee63aaa49566407819ca78cb250d
- id: cantina-op-token-bridge-2024-10
  type: audit_report
  title: Cantina MakerDAO OP Token Bridge Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/op-token-bridge/master/audit/20241023-cantina-report-review-makerdao-op-token-bridge.pdf
  path: audit-reports/cantina-op-token-bridge-2024-10.pdf
  date_published: '2024-10-23'
  date_checked: '2026-06-08'
  content_sha256: 1bfb87815c435588de9a76eb18a29cda8636a8aa7274729fbe84d96d86414685
```
