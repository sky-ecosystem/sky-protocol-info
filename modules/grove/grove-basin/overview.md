# grove-basin

## Codebases

```yaml
repositories:
- id: grove-basin
  name: grove-basin
  provider: github
  url: https://github.com/grove-labs/grove-basin
  ref: main
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/grove-basin/branch-main"
    checked_out_branch: main
    pinned_commit: d46291ae04833e71593860af32de2ad2c5a8ab90
```

## Deployments

```yaml
deployments: []
```

## Audit Reports

```yaml
audit_reports:
- id: cantina-grove-basin-audit
  auditor: Cantina
  report_title: Grove Basin Audit
  current_version: v100
  versions:
  - id: v100
    reference_refs:
    - cantina-grove-basin-audit-v100
    version_label: v1.0.0
    status: current
    audited_codebases:
    - grove-basin
    audited_sources:
    - codebase: grove-basin
      path: src/GroveBasin.sol
    - codebase: grove-basin
      path: src/GroveBasinFactory.sol
    - codebase: grove-basin
      path: src/pockets/AaveV3UsdtPocket.sol
    - codebase: grove-basin
      path: src/pockets/BasePocket.sol
    - codebase: grove-basin
      path: src/pockets/MorphoUsdtPocket.sol
    - codebase: grove-basin
      path: src/pockets/UsdsUsdcPocket.sol
    - codebase: grove-basin
      path: src/rate-providers/ChronicleRateProvider.sol
    - codebase: grove-basin
      path: src/rate-providers/FixedRateProvider.sol
    - codebase: grove-basin
      path: src/redeemers/BUIDLTokenRedeemer.sol
    - codebase: grove-basin
      path: src/redeemers/JTRSYTokenRedeemer.sol
    covered_contracts:
    - id: grove-basin
      name: GroveBasin
    - id: grove-basin-factory
      name: GroveBasinFactory
    - id: aave-v3-usdt-pocket
      name: AaveV3UsdtPocket
    - id: base-pocket
      name: BasePocket
    - id: morpho-usdt-pocket
      name: MorphoUsdtPocket
    - id: usds-usdc-pocket
      name: UsdsUsdcPocket
    - id: chronicle-rate-provider
      name: ChronicleRateProvider
    - id: fixed-rate-provider
      name: FixedRateProvider
    - id: buidl-token-redeemer
      name: BUIDLTokenRedeemer
    - id: jtrsy-token-redeemer
      name: JTRSYTokenRedeemer
- id: chainsecurity-grove-basin-audit
  auditor: ChainSecurity
  report_title: Basin Security Audit Report
  current_version: v100
  versions:
  - id: v100
    reference_refs:
    - chainsecurity-grove-basin-audit-v100
    version_label: v1.0.0
    status: current
    audited_codebases:
    - grove-basin
    audited_sources:
    - codebase: grove-basin
      path: src/GroveBasin.sol
    - codebase: grove-basin
      path: src/GroveBasinFactory.sol
    - codebase: grove-basin
      path: src/pockets/AaveV3UsdtPocket.sol
    - codebase: grove-basin
      path: src/pockets/BasePocket.sol
    - codebase: grove-basin
      path: src/pockets/MorphoUsdtPocket.sol
    - codebase: grove-basin
      path: src/pockets/UsdsUsdcPocket.sol
    - codebase: grove-basin
      path: src/rate-providers/ChronicleRateProvider.sol
    - codebase: grove-basin
      path: src/rate-providers/FixedRateProvider.sol
    - codebase: grove-basin
      path: src/redeemers/BUIDLTokenRedeemer.sol
    - codebase: grove-basin
      path: src/redeemers/JTRSYTokenRedeemer.sol
    covered_contracts:
    - id: grove-basin
      name: GroveBasin
    - id: grove-basin-factory
      name: GroveBasinFactory
    - id: aave-v3-usdt-pocket
      name: AaveV3UsdtPocket
    - id: base-pocket
      name: BasePocket
    - id: morpho-usdt-pocket
      name: MorphoUsdtPocket
    - id: usds-usdc-pocket
      name: UsdsUsdcPocket
    - id: chronicle-rate-provider
      name: ChronicleRateProvider
    - id: fixed-rate-provider
      name: FixedRateProvider
    - id: buidl-token-redeemer
      name: BUIDLTokenRedeemer
    - id: jtrsy-token-redeemer
      name: JTRSYTokenRedeemer
- id: riley-holterhus-grove-basin-audit
  auditor: Riley Holterhus
  report_title: Grove Basin Audit Report
  current_version: v100
  versions:
  - id: v100
    reference_refs:
    - riley-holterhus-grove-basin-audit-v100
    version_label: v1.0.0
    status: current
    audited_codebases:
    - grove-basin
    audited_sources:
    - codebase: grove-basin
      path: src/GroveBasin.sol
    - codebase: grove-basin
      path: src/GroveBasinFactory.sol
    - codebase: grove-basin
      path: src/pockets/AaveV3UsdtPocket.sol
    - codebase: grove-basin
      path: src/pockets/BasePocket.sol
    - codebase: grove-basin
      path: src/pockets/MorphoUsdtPocket.sol
    - codebase: grove-basin
      path: src/pockets/UsdsUsdcPocket.sol
    - codebase: grove-basin
      path: src/rate-providers/ChronicleRateProvider.sol
    - codebase: grove-basin
      path: src/rate-providers/FixedRateProvider.sol
    - codebase: grove-basin
      path: src/redeemers/BUIDLTokenRedeemer.sol
    - codebase: grove-basin
      path: src/redeemers/JTRSYTokenRedeemer.sol
    covered_contracts:
    - id: grove-basin
      name: GroveBasin
    - id: grove-basin-factory
      name: GroveBasinFactory
    - id: aave-v3-usdt-pocket
      name: AaveV3UsdtPocket
    - id: base-pocket
      name: BasePocket
    - id: morpho-usdt-pocket
      name: MorphoUsdtPocket
    - id: usds-usdc-pocket
      name: UsdsUsdcPocket
    - id: chronicle-rate-provider
      name: ChronicleRateProvider
    - id: fixed-rate-provider
      name: FixedRateProvider
    - id: buidl-token-redeemer
      name: BUIDLTokenRedeemer
    - id: jtrsy-token-redeemer
      name: JTRSYTokenRedeemer
references:
- id: cantina-grove-basin-audit-v100
  type: audit_report
  title: Cantina Grove Basin Audit
  url: https://raw.githubusercontent.com/grove-labs/grove-basin/d46291ae04833e71593860af32de2ad2c5a8ab90/audits/v100-cantina-audit.pdf
  path: audit-reports/cantina-grove-basin-audit-v100.pdf
  date_checked: '2026-06-10'
  content_sha256: 56cc624e98a09bf00500e1aca1604736731de82f9e76070b12e6beabf772317e
- id: chainsecurity-grove-basin-audit-v100
  type: audit_report
  title: ChainSecurity Basin Security Audit Report
  url: https://raw.githubusercontent.com/grove-labs/grove-basin/d46291ae04833e71593860af32de2ad2c5a8ab90/audits/v100-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-grove-basin-audit-v100.pdf
  date_checked: '2026-06-10'
  content_sha256: 83fb8f98e31cc723d7de5f24eb83868793ca2b04868a92dd05ea556da0a5e583
- id: riley-holterhus-grove-basin-audit-v100
  type: audit_report
  title: Riley Holterhus Grove Basin Audit Report
  url: https://raw.githubusercontent.com/grove-labs/grove-basin/d46291ae04833e71593860af32de2ad2c5a8ab90/audits/v100-riley-holterhus-audit.pdf
  path: audit-reports/riley-holterhus-grove-basin-audit-v100.pdf
  date_checked: '2026-06-10'
  content_sha256: 0a1a5b1853d89521119dc5e4061848cb034d1cbd3462c517bba4da23375b19e6
```

## Notes

```yaml
notes:
- No deployed addresses are recorded for this module.
```
