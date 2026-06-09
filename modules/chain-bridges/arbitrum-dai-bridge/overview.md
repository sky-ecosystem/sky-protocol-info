# arbitrum-dai-bridge

## Codebases

```yaml
repositories:
- id: arbitrum-dai-bridge
  name: arbitrum-dai-bridge
  provider: github
  url: https://github.com/sky-ecosystem/arbitrum-dai-bridge
  ref: master
  ref_type: branch
  source_code_roots:
  - contracts/l1
  - contracts/l2
  checkout:
    submodule_path: "./codebases/arbitrum-dai-bridge/branch-master"
    checked_out_branch: master
    pinned_commit: ba5e98631307025a74fc03108492b20af57a0d3a
```

## Deployments

```yaml
deployments:
- id: l1-dai-gateway-ethereum
  contract_id: l1-dai-gateway
  contract_name: L1DaiGateway
  status: live
  chain: Ethereum
  address: '0xD3B5b60020504bc3489D6949d545893982BA3011'
  implementation:
    codebase: arbitrum-dai-bridge
    submodule_path: "./codebases/arbitrum-dai-bridge/branch-master"
    source_path: contracts/l1/L1DaiGateway.sol
    contract_name: L1DaiGateway
    compiler:
      version: 0.6.11
      optimized: false
      evm_version: default
- id: l1-escrow-ethereum
  contract_id: l1-escrow
  contract_name: L1Escrow
  status: live
  chain: Ethereum
  address: '0xA10c7CE4b876998858b1a9E12b10092229539400'
  implementation:
    codebase: arbitrum-dai-bridge
    submodule_path: "./codebases/arbitrum-dai-bridge/branch-master"
    source_path: contracts/l1/L1Escrow.sol
    contract_name: L1Escrow
    compiler:
      version: 0.6.11
      optimized: false
      evm_version: default
- id: l1-governance-relay-ethereum
  contract_id: l1-governance-relay
  contract_name: L1GovernanceRelay
  status: live
  chain: Ethereum
  address: '0x9ba25c289e351779E0D481Ba37489317c34A899d'
  implementation:
    codebase: arbitrum-dai-bridge
    submodule_path: "./codebases/arbitrum-dai-bridge/branch-master"
    source_path: contracts/l1/L1GovernanceRelay.sol
    contract_name: L1GovernanceRelay
    compiler:
      version: 0.6.11
      optimized: false
      evm_version: default
- id: l2-dai-gateway-arbitrum
  contract_id: l2-dai-gateway
  contract_name: L2DaiGateway
  status: live
  chain: Arbitrum
  address: '0x467194771dAe2967Aef3ECbEDD3Bf9a310C76C65'
  implementation:
    codebase: arbitrum-dai-bridge
    submodule_path: "./codebases/arbitrum-dai-bridge/branch-master"
    source_path: contracts/l2/L2DaiGateway.sol
    contract_name: L2DaiGateway
- id: l2-governance-relay-arbitrum
  contract_id: l2-governance-relay
  contract_name: L2GovernanceRelay
  status: live
  chain: Arbitrum
  address: '0x10E6593CDda8c58a1d0f14C5164B376352a55f2F'
  implementation:
    codebase: arbitrum-dai-bridge
    submodule_path: "./codebases/arbitrum-dai-bridge/branch-master"
    source_path: contracts/l2/L2GovernanceRelay.sol
    contract_name: L2GovernanceRelay
- id: dai-l2-arbitrum
  contract_id: dai-l2
  contract_name: Dai (L2)
  status: live
  chain: Arbitrum
  address: '0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1'
  implementation:
    codebase: arbitrum-dai-bridge
    submodule_path: "./codebases/arbitrum-dai-bridge/branch-master"
    source_path: contracts/l2/dai.sol
    contract_name: Dai (L2)
```

## Audit Reports

```yaml
audit_reports: []
```
