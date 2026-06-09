# sky-oapp-oft

## Codebases

```yaml
repositories:
- id: sky-oapp-oft
  name: sky-oapp-oft
  provider: github
  url: https://github.com/sky-ecosystem/sky-oapp-oft
  ref: main
  ref_type: branch
  source_code_roots:
  - contracts
  checkout:
    submodule_path: "./branch-main"
    checked_out_branch: main
    pinned_commit: 0baba10c77a5cdfcef8fe9611e38d4306ab827a7
```

## Deployments

```yaml
deployments:
- id: governance-o-app-sender-ethereum
  contract_id: governance-o-app-sender
  contract_name: GovernanceOAppSender
  status: live
  chain: Ethereum
  address: '0x27FC1DD771817b53bE48Dc28789533BEa53C9CCA'
  implementation:
    codebase: sky-oapp-oft
    submodule_path: "./branch-main"
    source_path: contracts/GovernanceOAppSender.sol
    contract_name: GovernanceOAppSender
    compiler:
      version: 0.8.22
      optimized: true
      runs: 200
      evm_version: paris
- id: governance-o-app-receiver-avalanche
  contract_id: governance-o-app-receiver
  contract_name: GovernanceOAppReceiver
  status: live
  chain: Avalanche
  address: '0x6fdd46947ca6903c8c159d1dF2012Bc7fC5cEeec'
  implementation:
    codebase: sky-oapp-oft
    submodule_path: "./branch-main"
    source_path: contracts/GovernanceOAppReceiver.sol
    contract_name: GovernanceOAppReceiver
- id: sky-oft-adapter-ethereum
  contract_id: sky-oft-adapter
  contract_name: SkyOFTAdapter
  status: live
  chain: Ethereum
  address: '0x1e1D42781FC170EF9da004Fb735f56F0276d01B8'
  implementation:
    codebase: sky-oapp-oft
    submodule_path: "./branch-main"
    source_path: contracts/SkyOFTAdapter.sol
    contract_name: SkyOFTAdapter
    compiler:
      version: 0.8.22
      optimized: true
      runs: 200
      evm_version: paris
- id: sky-oft-adapter-mint-burn-usds-avalanche
  contract_id: sky-oft-adapter-mint-burn-usds
  contract_name: SkyOFTAdapterMintBurn(USDS)
  status: live
  chain: Avalanche
  address: '0x4fec40719fD9a8AE3F8E20531669DEC5962D2619'
  implementation:
    codebase: sky-oapp-oft
    submodule_path: "./branch-main"
    source_path: contracts/SkyOFTAdapterMintBurn.sol
    contract_name: SkyOFTAdapterMintBurn(USDS)
- id: sky-oft-adapter-mint-burn-s-usds-avalanche
  contract_id: sky-oft-adapter-mint-burn-s-usds
  contract_name: SkyOFTAdapterMintBurn(sUSDS)
  status: live
  chain: Avalanche
  address: '0x7297D4811f088FC26bC5475681405B99b41E1FF9'
  implementation:
    codebase: sky-oapp-oft
    submodule_path: "./branch-main"
    source_path: contracts/SkyOFTAdapterMintBurn.sol
    contract_name: SkyOFTAdapterMintBurn(sUSDS)
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-sky-governance-oapp
  auditor: ChainSecurity
  report_title: Sky Governance OApp Audit
  current_version: v2025-10
  versions:
  - id: v2025-10
    reference_refs:
    - chainsecurity-sky-governance-oapp-2025-10
    version_label: October 2025
    status: current
    audited_codebases:
    - sky-oapp-oft
    audited_sources:
    - codebase: sky-oapp-oft
      path: contracts/GovernanceOAppSender.sol
    - codebase: sky-oapp-oft
      path: contracts/GovernanceOAppReceiver.sol
    covered_contracts:
    - id: governance-o-app-sender
      name: GovernanceOAppSender
    - id: governance-o-app-receiver
      name: GovernanceOAppReceiver
- id: chainsecurity-sky-oapp-oft
  auditor: ChainSecurity
  report_title: Sky OApp OFT Audit
  current_version: v2025-10
  versions:
  - id: v2025-10
    reference_refs:
    - chainsecurity-sky-oapp-oft-2025-10
    version_label: October 2025
    status: current
    audited_codebases:
    - sky-oapp-oft
    audited_sources:
    - codebase: sky-oapp-oft
      path: contracts/SkyOFTAdapter.sol
    - codebase: sky-oapp-oft
      path: contracts/SkyOFTAdapterMintBurn.sol
    covered_contracts:
    - id: sky-oft-adapter
      name: SkyOFTAdapter
    - id: sky-oft-adapter-mint-burn-usds
      name: SkyOFTAdapterMintBurn(USDS)
    - id: sky-oft-adapter-mint-burn-s-usds
      name: SkyOFTAdapterMintBurn(sUSDS)
- id: cantina-sky-lz-governance-evm
  auditor: Cantina
  report_title: Sky LayerZero Governance EVM Audit
  current_version: v2025-09
  versions:
  - id: v2025-09
    reference_refs:
    - cantina-sky-lz-governance-evm-2025-09
    version_label: September 2025
    status: current
    audited_codebases:
    - sky-oapp-oft
    audited_sources:
    - codebase: sky-oapp-oft
      path: contracts/GovernanceOAppSender.sol
    - codebase: sky-oapp-oft
      path: contracts/GovernanceOAppReceiver.sol
    covered_contracts:
    - id: governance-o-app-sender
      name: GovernanceOAppSender
    - id: governance-o-app-receiver
      name: GovernanceOAppReceiver
- id: cantina-sky-lz-solana-governance
  auditor: Cantina
  report_title: Sky LayerZero Solana Governance Audit
  current_version: v2025-09
  versions:
  - id: v2025-09
    reference_refs:
    - cantina-sky-lz-solana-governance-2025-09
    version_label: September 2025
    status: current
    audited_codebases:
    - sky-oapp-oft
    scope_notes: Solana governance source files are not yet represented in this module's source_files records.
- id: cantina-sky-oft-evm
  auditor: Cantina
  report_title: Sky OFT EVM Audit
  current_version: v2025-09
  versions:
  - id: v2025-09
    reference_refs:
    - cantina-sky-oft-evm-2025-09
    version_label: September 2025
    status: current
    audited_codebases:
    - sky-oapp-oft
    audited_sources:
    - codebase: sky-oapp-oft
      path: contracts/SkyOFTAdapter.sol
    - codebase: sky-oapp-oft
      path: contracts/SkyOFTAdapterMintBurn.sol
    covered_contracts:
    - id: sky-oft-adapter
      name: SkyOFTAdapter
    - id: sky-oft-adapter-mint-burn-usds
      name: SkyOFTAdapterMintBurn(USDS)
    - id: sky-oft-adapter-mint-burn-s-usds
      name: SkyOFTAdapterMintBurn(sUSDS)
- id: cantina-sky-oft-solana
  auditor: Cantina
  report_title: Sky OFT Solana Audit
  current_version: v2025-09
  versions:
  - id: v2025-09
    reference_refs:
    - cantina-sky-oft-solana-2025-09
    version_label: September 2025
    status: current
    audited_codebases:
    - sky-oapp-oft
    scope_notes: Solana OFT source files are not yet represented in this module's source_files records.
- id: cantina-sky-oft-crosschain-gov-payloads
  auditor: Cantina
  report_title: Sky OFT Crosschain Governance Payloads Audit
  current_version: v2026-05
  versions:
  - id: v2026-05
    reference_refs:
    - cantina-sky-oft-crosschain-gov-payloads-2026-05
    version_label: May 2026
    status: current
    audited_codebases:
    - sky-oapp-oft
    scope_notes: Payload scope is recorded at module level until payload source records are added.
references:
- id: chainsecurity-sky-governance-oapp-2025-10
  type: audit_report
  title: ChainSecurity Sky Governance OApp Audit
  url: https://reports.chainsecurity.com/Sky/ChainSecurity_Sky_SkyGovernanceOApp_Audit.pdf
  path: audit-reports/chainsecurity-sky-governance-oapp-2025-10.pdf
  date_published: 2025-10
  date_checked: '2026-06-08'
  content_sha256: e19a278c928b85f8a0033e484b85db6ec9424037f3aa3321d461284362a54051
- id: chainsecurity-sky-oapp-oft-2025-10
  type: audit_report
  title: ChainSecurity Sky OApp OFT Audit
  url: https://reports.chainsecurity.com/Sky/ChainSecurity_Sky_SkyOAppOFT_Audit.pdf
  path: audit-reports/chainsecurity-sky-oapp-oft-2025-10.pdf
  date_published: 2025-10
  date_checked: '2026-06-08'
  content_sha256: a0be16ac7a7d2bf12c86d37e87c417bc63ace6c785505a83a601ddc95f29f8df
- id: cantina-sky-lz-governance-evm-2025-09
  type: audit_report
  title: Cantina Sky LayerZero Governance EVM Audit
  url: https://cdn.cantina.xyz/reports/cantina_sky_lz_governance_evm_sep2025.pdf
  path: audit-reports/cantina-sky-lz-governance-evm-2025-09.pdf
  date_published: 2025-09
  date_checked: '2026-06-08'
  content_sha256: c83236c5b593c8f34df348abc1773e4d73959ebdbd09da406cc8d2ff2a0bb12c
- id: cantina-sky-lz-solana-governance-2025-09
  type: audit_report
  title: Cantina Sky LayerZero Solana Governance Audit
  url: https://cdn.cantina.xyz/reports/cantina_sky_lz_solana_governance_sep2025.pdf
  path: audit-reports/cantina-sky-lz-solana-governance-2025-09.pdf
  date_published: 2025-09
  date_checked: '2026-06-08'
  content_sha256: 7cc58b623531c061b72e81073076e47e1f2418ceac953642f1c0f0dec2dc6fef
- id: cantina-sky-oft-evm-2025-09
  type: audit_report
  title: Cantina Sky OFT EVM Audit
  url: https://cdn.cantina.xyz/reports/cantina_sky_oft_evm_sep2025.pdf
  path: audit-reports/cantina-sky-oft-evm-2025-09.pdf
  date_published: 2025-09
  date_checked: '2026-06-08'
  content_sha256: 21d4c0651d7464e6db834cd82571d64c1a5d6247f3f586f56883bc77b90bdd9e
- id: cantina-sky-oft-solana-2025-09
  type: audit_report
  title: Cantina Sky OFT Solana Audit
  url: https://cdn.cantina.xyz/reports/cantina_sky_oft_solana_sep2025.pdf
  path: audit-reports/cantina-sky-oft-solana-2025-09.pdf
  date_published: 2025-09
  date_checked: '2026-06-08'
  content_sha256: ef3c82d8e492a22b4cdf262f1bdc4743ce4737d01fec9999a8bdb704ed44eba0
- id: cantina-sky-oft-crosschain-gov-payloads-2026-05
  type: audit_report
  title: Cantina Sky OFT Crosschain Governance Payloads Audit
  url: https://cdn.cantina.xyz/reports/cantina_sky_oft_crosschain_gov_payloads_may2026.pdf
  path: audit-reports/cantina-sky-oft-crosschain-gov-payloads-2026-05.pdf
  date_published: 2026-05
  date_checked: '2026-06-08'
  content_sha256: dd370d6f34de164951162e9eb80a2327efd9b6dfa10bd0b01d9663cde04de91a
reference_gaps:
- id: sky-oapp-oft-solana-source-records
  fact: Solana governance and OFT audit source coverage
  needed_reference: codebases.md source_files for programs/governance and programs/oft
  notes: Required before Solana audit reports can point at exact source file IDs.
```
