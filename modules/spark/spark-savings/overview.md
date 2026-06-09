# spark-savings

## Codebases

```yaml
repositories:
- id: spark-vaults-v2
  name: spark-vaults-v2
  provider: github
  url: https://github.com/sparkdotfi/spark-vaults-v2
  ref: dev
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/spark-vaults-v2/branch-dev"
    checked_out_branch: dev
    pinned_commit: 51c6d7a1da85944804ba87234f2eac13dba8330e
- id: spark-vaults
  name: spark-vaults
  provider: github
  url: https://github.com/sparkdotfi/spark-vaults
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/spark-vaults/branch-master"
    checked_out_branch: master
    pinned_commit: 78d37c8919f0d8c9943db02b9bca7077b6c38c10
- id: spark-savings-intents
  name: spark-savings-intents
  provider: github
  url: https://github.com/sparkdotfi/spark-savings-intents
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/spark-savings-intents/branch-master"
    checked_out_branch: master
    pinned_commit: 76005d9d83b1c8ee2174cd0ee95a799213c9ea8d
- id: spark-psm
  name: spark-psm
  provider: github
  url: https://github.com/sparkdotfi/spark-psm
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/spark-psm/branch-master"
    checked_out_branch: master
    pinned_commit: 2b1a72a7c24f95db0c4bda13ea9062ce9824577b
```

## Deployments

```yaml
deployments:
- id: spark-vault-v2-impl-ethereum
  contract_id: spark-vault-v2-impl
  contract_name: SparkVault
  status: live
  chain: Ethereum
  address: '0x1b992302652A92611DCd5090D1Cb388C6377f455'
  implementation:
    codebase: spark-vaults-v2
    submodule_path: "./codebases/spark-vaults-v2/branch-dev"
    source_path: src/SparkVault.sol
    contract_name: SparkVault
- id: spark-vault-v2-speth-ethereum
  contract_id: spark-vault-v2-speth
  contract_name: SparkVault
  status: live
  chain: Ethereum
  address: '0xfE6eb3b609a7C8352A241f7F3A21CEA4e9209B8f'
  implementation:
    codebase: spark-vaults-v2
    submodule_path: "./codebases/spark-vaults-v2/branch-dev"
    source_path: src/SparkVault.sol
    contract_name: SparkVault
- id: spark-vault-v2-sppyusd-ethereum
  contract_id: spark-vault-v2-sppyusd
  contract_name: SparkVault
  status: live
  chain: Ethereum
  address: '0x80128DbB9f07b93DDE62A6daeadb69ED14a7D354'
  implementation:
    codebase: spark-vaults-v2
    submodule_path: "./codebases/spark-vaults-v2/branch-dev"
    source_path: src/SparkVault.sol
    contract_name: SparkVault
- id: spark-vault-v2-spusdc-ethereum
  contract_id: spark-vault-v2-spusdc
  contract_name: SparkVault
  status: live
  chain: Ethereum
  address: '0x28B3a8fb53B741A8Fd78c0fb9A6B2393d896a43d'
  implementation:
    codebase: spark-vaults-v2
    submodule_path: "./codebases/spark-vaults-v2/branch-dev"
    source_path: src/SparkVault.sol
    contract_name: SparkVault
- id: spark-vault-v2-spusdt-ethereum
  contract_id: spark-vault-v2-spusdt
  contract_name: SparkVault
  status: live
  chain: Ethereum
  address: '0xe2e7a17dFf93280dec073C995595155283e3C372'
  implementation:
    codebase: spark-vaults-v2
    submodule_path: "./codebases/spark-vaults-v2/branch-dev"
    source_path: src/SparkVault.sol
    contract_name: SparkVault
- id: spark-savings-intents-ethereum
  contract_id: spark-savings-intents
  contract_name: SavingsVaultIntents
  status: live
  chain: Ethereum
  address: '0x592B7DB9906E6f8924C4D74c2A0aB86CE44fDDDf'
  implementation:
    codebase: spark-savings-intents
    submodule_path: "./codebases/spark-savings-intents/branch-master"
    source_path: src/SavingsVaultIntents.sol
    contract_name: SavingsVaultIntents
- id: susdc-ethereum
  contract_id: susdc
  contract_name: UsdcVault
  status: live
  chain: Ethereum
  address: '0xBc65ad17c5C0a2A4D159fa5a503f4992c7B545FE'
  implementation:
    codebase: spark-vaults
    submodule_path: "./codebases/spark-vaults/branch-master"
    source_path: src/UsdcVault.sol
    contract_name: UsdcVault
- id: psm3-base
  contract_id: psm3
  contract_name: PSM3
  status: live
  chain: Base
  address: '0x1601843c5E9bC251A3272907010AFa41Fa18347E'
  implementation:
    codebase: spark-psm
    submodule_path: "./codebases/spark-psm/branch-master"
    source_path: src/PSM3.sol
    contract_name: PSM3
- id: susdc-base
  contract_id: susdc
  contract_name: UsdcVaultL2
  status: live
  chain: Base
  address: '0x3128a0F7f0ea68E7B7c9B00AFa7E41045828e858'
  implementation:
    codebase: spark-vaults
    submodule_path: "./codebases/spark-vaults/branch-master"
    source_path: src/UsdcVaultL2.sol
    contract_name: UsdcVaultL2
- id: psm3-arbitrum-one
  contract_id: psm3
  contract_name: PSM3
  status: live
  chain: Arbitrum One
  address: '0x2B05F8e1cACC6974fD79A673a341Fe1f58d27266'
  implementation:
    codebase: spark-psm
    submodule_path: "./codebases/spark-psm/branch-master"
    source_path: src/PSM3.sol
    contract_name: PSM3
- id: susdc-arbitrum-one
  contract_id: susdc
  contract_name: UsdcVaultL2
  status: live
  chain: Arbitrum One
  address: '0x940098b108fB7D0a7E374f6eDED7760787464609'
  implementation:
    codebase: spark-vaults
    submodule_path: "./codebases/spark-vaults/branch-master"
    source_path: src/UsdcVaultL2.sol
    contract_name: UsdcVaultL2
- id: psm3-optimism
  contract_id: psm3
  contract_name: PSM3
  status: live
  chain: Optimism
  address: '0xe0F9978b907853F354d79188A3dEfbD41978af62'
  implementation:
    codebase: spark-psm
    submodule_path: "./codebases/spark-psm/branch-master"
    source_path: src/PSM3.sol
    contract_name: PSM3
- id: susdc-optimism
  contract_id: susdc
  contract_name: UsdcVaultL2
  status: live
  chain: Optimism
  address: '0xCF9326e24EBfFBEF22ce1050007A43A3c0B6DB55'
  implementation:
    codebase: spark-vaults
    submodule_path: "./codebases/spark-vaults/branch-master"
    source_path: src/UsdcVaultL2.sol
    contract_name: UsdcVaultL2
- id: psm3-unichain
  contract_id: psm3
  contract_name: PSM3
  status: live
  chain: Unichain
  address: '0x7b42Ed932f26509465F7cE3FAF76FfCe1275312f'
  implementation:
    codebase: spark-psm
    submodule_path: "./codebases/spark-psm/branch-master"
    source_path: src/PSM3.sol
    contract_name: PSM3
- id: susdc-unichain
  contract_id: susdc
  contract_name: UsdcVaultL2
  status: live
  chain: Unichain
  address: '0x14d9143BEcC348920b68D123687045db49a016C6'
  implementation:
    codebase: spark-vaults
    submodule_path: "./codebases/spark-vaults/branch-master"
    source_path: src/UsdcVaultL2.sol
    contract_name: UsdcVaultL2
- id: spark-vault-v2-impl-avalanche
  contract_id: spark-vault-v2-impl
  contract_name: SparkVault
  status: live
  chain: Avalanche
  address: '0xC2C0582D1cCe30449cF561C7b9C4D6d527547F12'
  implementation:
    codebase: spark-vaults-v2
    submodule_path: "./codebases/spark-vaults-v2/branch-dev"
    source_path: src/SparkVault.sol
    contract_name: SparkVault
- id: spark-vault-v2-spusdc-avalanche
  contract_id: spark-vault-v2-spusdc
  contract_name: SparkVault
  status: live
  chain: Avalanche
  address: '0x28B3a8fb53B741A8Fd78c0fb9A6B2393d896a43d'
  implementation:
    codebase: spark-vaults-v2
    submodule_path: "./codebases/spark-vaults-v2/branch-dev"
    source_path: src/SparkVault.sol
    contract_name: SparkVault
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-spark-psm-audit
  auditor: ChainSecurity
  report_title: Spark PSM Audit
  current_version: v2024-10-22
  versions:
  - id: v2024-10-22
    reference_refs:
    - chainsecurity-spark-psm-audit-2024-10-22
    version_label: 2024-10-22
    status: current
    audited_codebases:
    - spark-psm
    audited_sources:
    - codebase: spark-psm
      path: src/PSM3.sol
    covered_contracts:
    - id: psm3
      name: PSM3
- id: chainsecurity-spark-savings-intents-audit
  auditor: ChainSecurity
  report_title: Spark Savings Intents Audit
  current_version: v100
  versions:
  - id: v100
    reference_refs:
    - chainsecurity-spark-savings-intents-audit-v100
    version_label: v100
    status: current
    audited_codebases:
    - spark-savings-intents
    audited_sources:
    - codebase: spark-savings-intents
      path: src/SavingsVaultIntents.sol
    covered_contracts:
    - id: savings-vault-intents
      name: SavingsVaultIntents
- id: chainsecurity-spark-vaults-audit
  auditor: ChainSecurity
  report_title: Spark Vaults Audit
  current_version: v2025-01-24
  versions:
  - id: v2025-01-24
    reference_refs:
    - chainsecurity-spark-vaults-audit-2025-01-24
    version_label: 2025-01-24
    status: current
    audited_codebases:
    - spark-vaults
    audited_sources:
    - codebase: spark-vaults
      path: src/UsdcVault.sol
    - codebase: spark-vaults
      path: src/UsdcVaultL2.sol
    covered_contracts:
    - id: usdc-vault
      name: UsdcVault
    - id: usdc-vault-l2
      name: UsdcVaultL2
- id: chainsecurity-spark-vaults-v2-audit
  auditor: ChainSecurity
  report_title: Spark Vaults V2 Audit
  current_version: v101
  versions:
  - id: v101
    reference_refs:
    - chainsecurity-spark-vaults-v2-audit-v101
    version_label: v101
    status: current
    audited_codebases:
    - spark-vaults-v2
    audited_sources:
    - codebase: spark-vaults-v2
      path: src/SparkVault.sol
    covered_contracts:
    - id: spark-vault
      name: SparkVault
- id: cantina-spark-psm-audit
  auditor: Cantina
  report_title: Spark PSM Audit
  current_version: v2024-10-23
  versions:
  - id: v2024-10-23
    reference_refs:
    - cantina-spark-psm-audit-2024-10-23
    version_label: 2024-10-23
    status: current
    audited_codebases:
    - spark-psm
    audited_sources:
    - codebase: spark-psm
      path: src/PSM3.sol
    covered_contracts:
    - id: psm3
      name: PSM3
- id: cantina-spark-savings-intents-audit
  auditor: Cantina
  report_title: Spark Savings Intents Audit
  current_version: v100
  versions:
  - id: v100
    reference_refs:
    - cantina-spark-savings-intents-audit-v100
    version_label: v100
    status: current
    audited_codebases:
    - spark-savings-intents
    audited_sources:
    - codebase: spark-savings-intents
      path: src/SavingsVaultIntents.sol
    covered_contracts:
    - id: savings-vault-intents
      name: SavingsVaultIntents
- id: cantina-spark-vaults-audit
  auditor: Cantina
  report_title: Spark Vaults Audit
  current_version: v2025-02-26
  versions:
  - id: v2025-02-26
    reference_refs:
    - cantina-spark-vaults-audit-2025-02-26
    version_label: 2025-02-26
    status: current
    audited_codebases:
    - spark-vaults
    audited_sources:
    - codebase: spark-vaults
      path: src/UsdcVault.sol
    - codebase: spark-vaults
      path: src/UsdcVaultL2.sol
    covered_contracts:
    - id: usdc-vault
      name: UsdcVault
    - id: usdc-vault-l2
      name: UsdcVaultL2
- id: cantina-spark-vaults-v2-audit
  auditor: Cantina
  report_title: Spark Vaults V2 Audit
  current_version: v101
  versions:
  - id: v101
    reference_refs:
    - cantina-spark-vaults-v2-audit-v101
    version_label: v101
    status: current
    audited_codebases:
    - spark-vaults-v2
    audited_sources:
    - codebase: spark-vaults-v2
      path: src/SparkVault.sol
    covered_contracts:
    - id: spark-vault
      name: SparkVault
references:
- id: chainsecurity-spark-psm-audit-2024-10-22
  type: audit_report
  title: ChainSecurity Spark PSM Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-psm/2b1a72a7c24f95db0c4bda13ea9062ce9824577b/audits/20241022-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-spark-psm-audit-2024-10-22.pdf
  date_published: '2024-10-22'
  date_checked: '2026-06-09'
  content_sha256: 05e18d3134b3838c172815b73e60a47075059acd4b519772310ea29a02df37e3
- id: chainsecurity-spark-savings-intents-audit-v100
  type: audit_report
  title: ChainSecurity Spark Savings Intents Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-savings-intents/76005d9d83b1c8ee2174cd0ee95a799213c9ea8d/audits/v100-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-spark-savings-intents-audit-v100.pdf
  date_checked: '2026-06-09'
  content_sha256: d942f4d68bb5b6620fb8727cb0b7655e04bb2fdb5e2f02311cb495564ae78d96
- id: chainsecurity-spark-vaults-audit-2025-01-24
  type: audit_report
  title: ChainSecurity Spark Vaults Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-vaults/78d37c8919f0d8c9943db02b9bca7077b6c38c10/audits/20250124-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-spark-vaults-audit-2025-01-24.pdf
  date_published: '2025-01-24'
  date_checked: '2026-06-09'
  content_sha256: f2d3839278a05f3ca4c2c19b3146b86bdda6f05022139d16b5b61d136df73e9e
- id: chainsecurity-spark-vaults-v2-audit-v101
  type: audit_report
  title: ChainSecurity Spark Vaults V2 Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-vaults-v2/51c6d7a1da85944804ba87234f2eac13dba8330e/audits/v101-chainsecurity.pdf
  path: audit-reports/chainsecurity-spark-vaults-v2-audit-v101.pdf
  date_checked: '2026-06-09'
  content_sha256: 5d7ce3ee597bcf87820adaff73efc2e5de5dd0606beec4f2cd404f1dffe49e6a
- id: cantina-spark-psm-audit-2024-10-23
  type: audit_report
  title: Cantina Spark PSM Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-psm/2b1a72a7c24f95db0c4bda13ea9062ce9824577b/audits/20241023-cantina-audit.pdf
  path: audit-reports/cantina-spark-psm-audit-2024-10-23.pdf
  date_published: '2024-10-23'
  date_checked: '2026-06-09'
  content_sha256: ab73ac27483e4ea6e33c6bf3ab72db4f5ab0b6591ae393eb21b06bfd75d91edf
- id: cantina-spark-savings-intents-audit-v100
  type: audit_report
  title: Cantina Spark Savings Intents Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-savings-intents/76005d9d83b1c8ee2174cd0ee95a799213c9ea8d/audits/v100-cantina-audit.pdf
  path: audit-reports/cantina-spark-savings-intents-audit-v100.pdf
  date_checked: '2026-06-09'
  content_sha256: f792ce552c8ad91570968beea2bb4a28ad460e9cf98e44982dfa633c26eeeb1c
- id: cantina-spark-vaults-audit-2025-02-26
  type: audit_report
  title: Cantina Spark Vaults Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-vaults/78d37c8919f0d8c9943db02b9bca7077b6c38c10/audits/20250226-cantina-audit.pdf
  path: audit-reports/cantina-spark-vaults-audit-2025-02-26.pdf
  date_published: '2025-02-26'
  date_checked: '2026-06-09'
  content_sha256: 82d09640476e39ac9e80f376d682772bd3629516a9cf2a0d6006452e69700079
- id: cantina-spark-vaults-v2-audit-v101
  type: audit_report
  title: Cantina Spark Vaults V2 Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-vaults-v2/51c6d7a1da85944804ba87234f2eac13dba8330e/audits/v101-cantina.pdf
  path: audit-reports/cantina-spark-vaults-v2-audit-v101.pdf
  date_checked: '2026-06-09'
  content_sha256: 8a1c0397e61e58aab1a14711683860d0dc6d31f31b18e699be09be55e5c9372f
```

## Notes
