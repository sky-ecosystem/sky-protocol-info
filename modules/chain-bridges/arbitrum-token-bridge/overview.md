# arbitrum-token-bridge

## Codebases

```yaml
repositories:
- id: arbitrum-token-bridge
  name: arbitrum-token-bridge
  provider: github
  url: https://github.com/sky-ecosystem/arbitrum-token-bridge
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/arbitrum-token-bridge/branch-master"
    checked_out_branch: master
    pinned_commit: beb73666df3e7d15797720c6bdabad5b554678e8
```

## Deployments

```yaml
deployments:
- id: l1-token-gateway-ethereum
  contract_id: l1-token-gateway
  contract_name: L1TokenGateway
  status: live
  chain: Ethereum
  address: '0x12eDe82637d5507026D4CDb3515B4b022Ed157b1'
  implementation:
    codebase: arbitrum-token-bridge
    submodule_path: "./codebases/arbitrum-token-bridge/branch-master"
    source_path: src/L1TokenGateway.sol
    contract_name: L1TokenGateway
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
- id: l2-token-gateway-arbitrum
  contract_id: l2-token-gateway
  contract_name: L2TokenGateway
  status: live
  chain: Arbitrum
  address: '0xD404eD36D6976BdCad8ABbcCC9F09ef07e33A9A8'
  implementation:
    codebase: arbitrum-token-bridge
    submodule_path: "./codebases/arbitrum-token-bridge/branch-master"
    source_path: src/L2TokenGateway.sol
    contract_name: L2TokenGateway
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-arbitrum-token-bridge
  auditor: ChainSecurity
  report_title: MakerDAO Arbitrum Token Bridge Audit
  current_version: v2024-10
  versions:
  - id: v2024-10
    reference_refs:
    - chainsecurity-arbitrum-token-bridge-2024-10
    version_label: October 2024
    status: current
    audited_codebases:
    - arbitrum-token-bridge
    audited_sources:
    - codebase: arbitrum-token-bridge
      path: src/L1TokenGateway.sol
    - codebase: arbitrum-token-bridge
      path: src/L2TokenGateway.sol
    covered_contracts:
    - id: l1-token-gateway
      name: L1TokenGateway
    - id: l2-token-gateway
      name: L2TokenGateway
- id: cantina-arbitrum-token-bridge
  auditor: Cantina
  report_title: MakerDAO Arbitrum Token Bridge Audit
  current_version: v2024-10
  versions:
  - id: v2024-07
    reference_refs:
    - cantina-arbitrum-token-bridge-2024-07
    version_label: July 2024
    status: superseded
    superseded_by: v2024-10
    audited_codebases:
    - arbitrum-token-bridge
    audited_sources:
    - codebase: arbitrum-token-bridge
      path: src/L1TokenGateway.sol
    - codebase: arbitrum-token-bridge
      path: src/L2TokenGateway.sol
    covered_contracts:
    - id: l1-token-gateway
      name: L1TokenGateway
    - id: l2-token-gateway
      name: L2TokenGateway
  - id: v2024-10
    reference_refs:
    - cantina-arbitrum-token-bridge-2024-10
    version_label: October 2024
    status: current
    supersedes:
    - v2024-07
    audited_codebases:
    - arbitrum-token-bridge
    audited_sources:
    - codebase: arbitrum-token-bridge
      path: src/L1TokenGateway.sol
    - codebase: arbitrum-token-bridge
      path: src/L2TokenGateway.sol
    covered_contracts:
    - id: l1-token-gateway
      name: L1TokenGateway
    - id: l2-token-gateway
      name: L2TokenGateway
references:
- id: chainsecurity-arbitrum-token-bridge-2024-10
  type: audit_report
  title: ChainSecurity MakerDAO Arbitrum Token Bridge Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/arbitrum-token-bridge/master/audit/20241009-ChainSecurity_MakerDAO_Arbitrum_Token_Bridge_audit.pdf
  path: audit-reports/chainsecurity-arbitrum-token-bridge-2024-10.pdf
  date_published: '2024-10-09'
  date_checked: '2026-06-08'
  content_sha256: 8312f2b3035ae0c66f8aca56ff6f8cdbbe74950743575078407a959fb9c1892f
- id: cantina-arbitrum-token-bridge-2024-07
  type: audit_report
  title: Cantina MakerDAO Arbitrum Token Bridge Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/arbitrum-token-bridge/master/audit/20240703-cantina-report-maker-arbitrum-token-bridge.pdf
  path: audit-reports/cantina-arbitrum-token-bridge-2024-07.pdf
  date_published: '2024-07-03'
  date_checked: '2026-06-08'
  content_sha256: 1da8a66ed63826c341e0eb43fb0e6154f0a51e06cdf0d5bc8cc858c83d529ea0
- id: cantina-arbitrum-token-bridge-2024-10
  type: audit_report
  title: Cantina MakerDAO Arbitrum Token Bridge Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/arbitrum-token-bridge/master/audit/20241023-cantina-report-maker-arbitrum-token-bridge.pdf
  path: audit-reports/cantina-arbitrum-token-bridge-2024-10.pdf
  date_published: '2024-10-23'
  date_checked: '2026-06-08'
  content_sha256: 3a88d0d58124d075333abe8a48ef24c3941da5a70434c8a35757f4334bc2b196
```
