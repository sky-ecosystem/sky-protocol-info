# spark-rewards

## Codebases

```yaml
repositories:
- id: spark-rewards
  name: spark-rewards
  provider: github
  url: https://github.com/sparkdotfi/spark-rewards
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/spark-rewards/branch-master"
    checked_out_branch: master
    pinned_commit: 77bc191d027d33399440c49831a4f6700ccfe7b7
```

## Deployments

```yaml
deployments:
- id: cookie3-rewards-ethereum
  contract_id: cookie3-rewards
  contract_name: SparkRewards
  status: live
  chain: Ethereum
  address: '0x9107F5f940226A9f21433F373A4f938228d20e1A'
  implementation:
    codebase: spark-rewards
    submodule_path: "./codebases/spark-rewards/branch-master"
    source_path: src/SparkRewards.sol
    contract_name: SparkRewards
- id: ignition-rewards-ethereum
  contract_id: ignition-rewards
  contract_name: SparkRewards
  status: live
  chain: Ethereum
  address: '0xCBA0C0a2a0B6Bb11233ec4EA85C5bFfea33e724d'
  implementation:
    codebase: spark-rewards
    submodule_path: "./codebases/spark-rewards/branch-master"
    source_path: src/SparkRewards.sol
    contract_name: SparkRewards
- id: pfl3-rewards-ethereum
  contract_id: pfl3-rewards
  contract_name: SparkRewards
  status: live
  chain: Ethereum
  address: '0x7ac96180C4d6b2A328D3a19ac059D0E7Fc3C6d41'
  implementation:
    codebase: spark-rewards
    submodule_path: "./codebases/spark-rewards/branch-master"
    source_path: src/SparkRewards.sol
    contract_name: SparkRewards
- id: points-rewards-ethereum
  contract_id: points-rewards
  contract_name: SparkRewards
  status: live
  chain: Ethereum
  address: '0xe9eaE48Ed66C63fD4D12e315BC7d31Aacd89a909'
  implementation:
    codebase: spark-rewards
    submodule_path: "./codebases/spark-rewards/branch-master"
    source_path: src/SparkRewards.sol
    contract_name: SparkRewards
- id: spark-rewards-ethereum
  contract_id: spark-rewards
  contract_name: SparkRewards
  status: live
  chain: Ethereum
  address: '0xbaf21A27622Db71041Bd336a573DDEdC8eB65122'
  implementation:
    codebase: spark-rewards
    submodule_path: "./codebases/spark-rewards/branch-master"
    source_path: src/SparkRewards.sol
    contract_name: SparkRewards
- id: spark-rewards-optimism
  contract_id: spark-rewards
  contract_name: SparkRewards
  status: live
  chain: Optimism
  address: '0xf94473Bf6EF648638A7b1eEef354fE440721ef41'
  implementation:
    codebase: spark-rewards
    submodule_path: "./codebases/spark-rewards/branch-master"
    source_path: src/SparkRewards.sol
    contract_name: SparkRewards
- id: spark-rewards-avalanche
  contract_id: spark-rewards
  contract_name: SparkRewards
  status: live
  chain: Avalanche
  address: '0xAf76856f788519704a9411839614e144FEd52d8a'
  implementation:
    codebase: spark-rewards
    submodule_path: "./codebases/spark-rewards/branch-master"
    source_path: src/SparkRewards.sol
    contract_name: SparkRewards
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-spark-rewards-audit
  auditor: ChainSecurity
  report_title: Spark Rewards Audit
  current_version: v2025-02-25
  versions:
  - id: v2025-02-25
    reference_refs:
    - chainsecurity-spark-rewards-audit-2025-02-25
    version_label: 2025-02-25
    status: current
    audited_codebases:
    - spark-rewards
    audited_sources:
    - codebase: spark-rewards
      path: src/SparkRewards.sol
    covered_contracts:
    - id: spark-rewards
      name: SparkRewards
- id: cantina-spark-rewards-audit
  auditor: Cantina
  report_title: Spark Rewards Audit
  current_version: v2025-02-27
  versions:
  - id: v2025-02-27
    reference_refs:
    - cantina-spark-rewards-audit-2025-02-27
    version_label: 2025-02-27
    status: current
    audited_codebases:
    - spark-rewards
    audited_sources:
    - codebase: spark-rewards
      path: src/SparkRewards.sol
    covered_contracts:
    - id: spark-rewards
      name: SparkRewards
references:
- id: chainsecurity-spark-rewards-audit-2025-02-25
  type: audit_report
  title: ChainSecurity Spark Rewards Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-rewards/77bc191d027d33399440c49831a4f6700ccfe7b7/audits/20250225-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-spark-rewards-audit-2025-02-25.pdf
  date_published: '2025-02-25'
  date_checked: '2026-06-09'
  content_sha256: 55f8117733700feaba800c9e5d4c8a0c138417a399b838cc104a45db5e820994
- id: cantina-spark-rewards-audit-2025-02-27
  type: audit_report
  title: Cantina Spark Rewards Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-rewards/77bc191d027d33399440c49831a4f6700ccfe7b7/audits/20250227-cantina-audit.pdf
  path: audit-reports/cantina-spark-rewards-audit-2025-02-27.pdf
  date_published: '2025-02-27'
  date_checked: '2026-06-09'
  content_sha256: 226d5a1bb18cfd0402ceef727e7eeea5314188b671210a3e6277a988ef99dd8c
```

## Notes
