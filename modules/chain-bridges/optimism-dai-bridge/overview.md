# optimism-dai-bridge

## Codebases

```yaml
repositories:
- id: optimism-dai-bridge
  name: optimism-dai-bridge
  provider: github
  url: https://github.com/sky-ecosystem/optimism-dai-bridge
  ref: master
  ref_type: branch
  source_code_roots:
  - contracts/l1
  - contracts/l2
  checkout:
    submodule_path: "./codebases/optimism-dai-bridge/branch-master"
    checked_out_branch: master
    pinned_commit: bc3d63f5da2fd34ebb90369c90f2ea57e51cbca0
```

## Deployments

```yaml
deployments:
- id: l1-dai-token-bridge-ethereum
  contract_id: l1-dai-token-bridge
  contract_name: L1DAITokenBridge
  status: live
  chain: Ethereum
  address: '0x10E6593CDda8c58a1d0f14C5164B376352a55f2F'
  implementation:
    codebase: optimism-dai-bridge
    submodule_path: "./codebases/optimism-dai-bridge/branch-master"
    source_path: contracts/l1/L1DAITokenBridge.sol
    contract_name: L1DAITokenBridge
    compiler:
      version: 0.7.6
      optimized: false
      evm_version: default
- id: l1-governance-relay-ethereum
  contract_id: l1-governance-relay
  contract_name: L1GovernanceRelay
  status: live
  chain: Ethereum
  address: '0x09B354CDA89203BB7B3131CC728dFa06ab09Ae2F'
  implementation:
    codebase: optimism-dai-bridge
    submodule_path: "./codebases/optimism-dai-bridge/branch-master"
    source_path: contracts/l1/L1GovernanceRelay.sol
    contract_name: L1GovernanceRelay
    compiler:
      version: 0.7.6
      optimized: false
      evm_version: default
- id: l1-escrow-ethereum
  contract_id: l1-escrow
  contract_name: L1Escrow
  status: live
  chain: Ethereum
  address: '0x467194771dAe2967Aef3ECbEDD3Bf9a310C76C65'
  implementation:
    codebase: optimism-dai-bridge
    submodule_path: "./codebases/optimism-dai-bridge/branch-master"
    source_path: contracts/l1/L1Escrow.sol
    contract_name: L1Escrow
    compiler:
      version: 0.7.6
      optimized: false
      evm_version: default
- id: l2-dai-token-bridge-optimism
  contract_id: l2-dai-token-bridge
  contract_name: L2DAITokenBridge
  status: live
  chain: Optimism
  address: '0x467194771dAe2967Aef3ECbEDD3Bf9a310C76C65'
  implementation:
    codebase: optimism-dai-bridge
    submodule_path: "./codebases/optimism-dai-bridge/branch-master"
    source_path: contracts/l2/L2DAITokenBridge.sol
    contract_name: L2DAITokenBridge
- id: l2-governance-relay-optimism
  contract_id: l2-governance-relay
  contract_name: L2GovernanceRelay
  status: live
  chain: Optimism
  address: '0x10E6593CDda8c58a1d0f14C5164B376352a55f2F'
  implementation:
    codebase: optimism-dai-bridge
    submodule_path: "./codebases/optimism-dai-bridge/branch-master"
    source_path: contracts/l2/L2GovernanceRelay.sol
    contract_name: L2GovernanceRelay
- id: dai-l2-optimism
  contract_id: dai-l2
  contract_name: Dai (L2)
  status: live
  chain: Optimism
  address: '0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1'
  implementation:
    codebase: optimism-dai-bridge
    submodule_path: "./codebases/optimism-dai-bridge/branch-master"
    source_path: contracts/l2/dai.sol
    contract_name: Dai (L2)
```

## Audit Reports

```yaml
audit_reports: []
```
