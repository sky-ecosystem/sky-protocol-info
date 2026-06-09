# spark-governance

## Codebases

```yaml
repositories:
- id: spark-gov-relay
  name: spark-gov-relay
  provider: github
  url: https://github.com/sparkdotfi/spark-gov-relay
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/spark-gov-relay/branch-master"
    checked_out_branch: master
    pinned_commit: 6218d57c203568f45ff28d00f41076f2a3d9e0e6
- id: xchain-helpers-commit-33baf1e
  name: xchain-helpers
  provider: github
  url: https://github.com/marsfoundation/xchain-helpers
  ref: 33baf1e96833cb0d1de0ca57c115459b76565fd4
  ref_type: commit
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/xchain-helpers/commit-33baf1e"
    checked_out_branch: HEAD
    pinned_commit: 33baf1e96833cb0d1de0ca57c115459b76565fd4
```

## Deployments

```yaml
deployments:
- id: spark-executor-base
  contract_id: spark-executor
  contract_name: Executor
  status: live
  chain: Base
  address: '0xF93B7122450A50AF3e5A76E1d546e95Ac1d0F579'
  implementation:
    codebase: spark-gov-relay
    submodule_path: "./codebases/spark-gov-relay/branch-master"
    source_path: src/Executor.sol
    contract_name: Executor
- id: spark-receiver-base
  contract_id: spark-receiver
  contract_name: OptimismReceiver
  status: live
  chain: Base
  address: '0xfda082e00EF89185d9DB7E5DcD8c5505070F5A3B'
  implementation:
    codebase: xchain-helpers-commit-33baf1e
    submodule_path: "./codebases/xchain-helpers/commit-33baf1e"
    source_path: src/receivers/OptimismReceiver.sol
    contract_name: OptimismReceiver
- id: spark-executor-arbitrum-one
  contract_id: spark-executor
  contract_name: Executor
  status: live
  chain: Arbitrum One
  address: '0x65d946e533748A998B1f0E430803e39A6388f7a1'
  implementation:
    codebase: spark-gov-relay
    submodule_path: "./codebases/spark-gov-relay/branch-master"
    source_path: src/Executor.sol
    contract_name: Executor
- id: spark-receiver-arbitrum-one
  contract_id: spark-receiver
  contract_name: ArbitrumReceiver
  status: live
  chain: Arbitrum One
  address: '0x212871A1C235892F86cAB30E937e18c94AEd8474'
  implementation:
    codebase: xchain-helpers-commit-33baf1e
    submodule_path: "./codebases/xchain-helpers/commit-33baf1e"
    source_path: src/receivers/ArbitrumReceiver.sol
    contract_name: ArbitrumReceiver
- id: spark-executor-optimism
  contract_id: spark-executor
  contract_name: Executor
  status: live
  chain: Optimism
  address: '0x205216D89a00FeB2a73273ceecD297BAf89d576d'
  implementation:
    codebase: spark-gov-relay
    submodule_path: "./codebases/spark-gov-relay/branch-master"
    source_path: src/Executor.sol
    contract_name: Executor
- id: spark-receiver-optimism
  contract_id: spark-receiver
  contract_name: OptimismReceiver
  status: live
  chain: Optimism
  address: '0x61Baf0Ce69D23C8318c786e161D1cAc285AA4EA3'
  implementation:
    codebase: xchain-helpers-commit-33baf1e
    submodule_path: "./codebases/xchain-helpers/commit-33baf1e"
    source_path: src/receivers/OptimismReceiver.sol
    contract_name: OptimismReceiver
- id: spark-executor-unichain
  contract_id: spark-executor
  contract_name: Executor
  status: live
  chain: Unichain
  address: '0xb037C43b433964A2017cd689f535BEb6B0531473'
  implementation:
    codebase: spark-gov-relay
    submodule_path: "./codebases/spark-gov-relay/branch-master"
    source_path: src/Executor.sol
    contract_name: Executor
- id: spark-receiver-unichain
  contract_id: spark-receiver
  contract_name: OptimismReceiver
  status: live
  chain: Unichain
  address: '0x7B8ee8b0fD62662F7FB1ac9e5E6cEAad5195A3bF'
  implementation:
    codebase: xchain-helpers-commit-33baf1e
    submodule_path: "./codebases/xchain-helpers/commit-33baf1e"
    source_path: src/receivers/OptimismReceiver.sol
    contract_name: OptimismReceiver
- id: spark-executor-avalanche
  contract_id: spark-executor
  contract_name: Executor
  status: live
  chain: Avalanche
  address: '0x7566DEbC906C17338524A414343fA61BcA26A843'
  implementation:
    codebase: spark-gov-relay
    submodule_path: "./codebases/spark-gov-relay/branch-master"
    source_path: src/Executor.sol
    contract_name: Executor
- id: spark-receiver-avalanche
  contract_id: spark-receiver
  contract_name: LZReceiver
  status: live
  chain: Avalanche
  address: '0xd905be48983D405C6fD7f5a983D2351fb61C691F'
  implementation:
    codebase: xchain-helpers-commit-33baf1e
    submodule_path: "./codebases/xchain-helpers/commit-33baf1e"
    source_path: src/receivers/LZReceiver.sol
    contract_name: LZReceiver
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-spark-gov-relay-audit
  auditor: ChainSecurity
  report_title: Spark Gov Relay Audit
  current_version: v100
  versions:
  - id: v100
    reference_refs:
    - chainsecurity-spark-gov-relay-audit-v100
    version_label: v100
    status: current
    audited_codebases:
    - spark-gov-relay
    audited_sources:
    - codebase: spark-gov-relay
      path: src/Executor.sol
    covered_contracts:
    - id: executor
      name: Executor
- id: chainsecurity-sparkdao-xchain-helpers-audit
  auditor: ChainSecurity
  report_title: SparkDAO Xchain Helpers Audit
  current_version: final
  versions:
  - id: final
    reference_refs:
    - chainsecurity-sparkdao-xchain-helpers-audit-final
    version_label: Final
    status: current
    audited_codebases:
    - xchain-helpers-commit-33baf1e
    audited_sources:
    - codebase: xchain-helpers-commit-33baf1e
      path: src/receivers/ArbitrumReceiver.sol
    - codebase: xchain-helpers-commit-33baf1e
      path: src/receivers/LZReceiver.sol
    - codebase: xchain-helpers-commit-33baf1e
      path: src/receivers/OptimismReceiver.sol
    covered_contracts:
    - id: arbitrum-receiver
      name: ArbitrumReceiver
    - id: lz-receiver
      name: LZReceiver
    - id: optimism-receiver
      name: OptimismReceiver
- id: cantina-xchain-helpers-spark-gov-relay-review
  auditor: Cantina
  report_title: Xchain Helpers / Spark Gov Relay Review
  current_version: final
  versions:
  - id: final
    reference_refs:
    - cantina-xchain-helpers-spark-gov-relay-review-final
    version_label: Final
    status: current
    audited_codebases:
    - spark-gov-relay
    - xchain-helpers-commit-33baf1e
    audited_sources:
    - codebase: spark-gov-relay
      path: src/Executor.sol
    - codebase: xchain-helpers-commit-33baf1e
      path: src/receivers/ArbitrumReceiver.sol
    - codebase: xchain-helpers-commit-33baf1e
      path: src/receivers/LZReceiver.sol
    - codebase: xchain-helpers-commit-33baf1e
      path: src/receivers/OptimismReceiver.sol
    covered_contracts:
    - id: arbitrum-receiver
      name: ArbitrumReceiver
    - id: executor
      name: Executor
    - id: lz-receiver
      name: LZReceiver
    - id: optimism-receiver
      name: OptimismReceiver
references:
- id: chainsecurity-spark-gov-relay-audit-v100
  type: audit_report
  title: ChainSecurity Spark Gov Relay Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-gov-relay/6218d57c203568f45ff28d00f41076f2a3d9e0e6/audits/v100-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-spark-gov-relay-audit-v100.pdf
  date_checked: '2026-06-09'
  content_sha256: 599c1eb96254c67127054bc90d1c18117273edaaa5af032bc685616f91f71b97
- id: chainsecurity-sparkdao-xchain-helpers-audit-final
  type: audit_report
  title: ChainSecurity SparkDAO Xchain Helpers Audit
  url: https://raw.githubusercontent.com/marsfoundation/xchain-helpers/33baf1e96833cb0d1de0ca57c115459b76565fd4/audits/ChainSecurity_SparkDAO_xchain-helpers_audit.pdf
  path: audit-reports/chainsecurity-sparkdao-xchain-helpers-audit-final.pdf
  date_checked: '2026-06-09'
  content_sha256: b6b23c79fff10a5f73df90403d53da9681d19e02ae1e40dff40fb8495e30ebb6
- id: cantina-xchain-helpers-spark-gov-relay-review-final
  type: audit_report
  title: Cantina Xchain Helpers / Spark Gov Relay Review
  url: https://raw.githubusercontent.com/marsfoundation/xchain-helpers/33baf1e96833cb0d1de0ca57c115459b76565fd4/audits/report-review-makerdao-xchain-helpers-spark-gov-relay.pdf
  path: audit-reports/cantina-xchain-helpers-spark-gov-relay-review-final.pdf
  date_checked: '2026-06-09'
  content_sha256: c4917619294e8bfb5487f6a3cacc4b9d98ef59148aa707f1c8b5ff7b415aa8eb
```

## Notes
