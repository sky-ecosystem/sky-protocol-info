# dss

## Codebases

```yaml
repositories:
- id: dss-master
  name: dss
  provider: github
  url: https://github.com/sky-ecosystem/dss
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: fa4f6630afb0624d04a003e920b0d71a00331d98
- id: dss-v1-2
  name: dss
  provider: github
  url: https://github.com/sky-ecosystem/dss
  ref: v1.2
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-v1.2"
    checked_out_branch: v1.2
    pinned_commit: 38f618c54ff27d278eacc58d543e01bd08a88680
```

## Deployments

```yaml
deployments:
- id: vat-ethereum
  contract_id: vat
  contract_name: Vat
  status: live
  chain: Ethereum
  address: '0x35D1b3F3D7966A1DFe207aa4514C12a259A0492B'
  implementation:
    codebase: dss-v1-2
    submodule_path: "./branch-v1.2"
    source_path: src/vat.sol
    contract_name: Vat
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
- id: vow-ethereum
  contract_id: vow
  contract_name: Vow
  status: live
  chain: Ethereum
  address: '0xA950524441892A31ebddF91d3cEEFa04Bf454466'
  implementation:
    codebase: dss-v1-2
    submodule_path: "./branch-v1.2"
    source_path: src/vow.sol
    contract_name: Vow
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
- id: spotter-ethereum
  contract_id: spotter
  contract_name: Spotter
  status: live
  chain: Ethereum
  address: '0x65C79fcB50Ca1594B025960e539eD7A9a6D434A3'
  implementation:
    codebase: dss-v1-2
    submodule_path: "./branch-v1.2"
    source_path: src/spot.sol
    contract_name: Spotter
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
- id: jug-ethereum
  contract_id: jug
  contract_name: Jug
  status: live
  chain: Ethereum
  address: '0x19c0976f590D67707E62397C87829d896Dc0f1F1'
  implementation:
    codebase: dss-v1-2
    submodule_path: "./branch-v1.2"
    source_path: src/jug.sol
    contract_name: Jug
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
- id: dai-ethereum
  contract_id: dai
  contract_name: Dai
  status: live
  chain: Ethereum
  address: '0x6B175474E89094C44Da98b954EedeAC495271d0F'
  implementation:
    codebase: dss-v1-2
    submodule_path: "./branch-v1.2"
    source_path: src/dai.sol
    contract_name: Dai
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
- id: dai-join-ethereum
  contract_id: dai-join
  contract_name: DaiJoin
  status: live
  chain: Ethereum
  address: '0x9759A6Ac90977b93B58547b4A71c78317f391A28'
  implementation:
    codebase: dss-v1-2
    submodule_path: "./branch-v1.2"
    source_path: src/join.sol
    contract_name: DaiJoin
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
- id: gem-join-ethereum
  contract_id: gem-join
  contract_name: GemJoin
  status: live
  chain: Ethereum
  address: '0x2F0b23f53734252Bda2277357e97e1517d6B042A'
  implementation:
    codebase: dss-v1-2
    submodule_path: "./branch-v1.2"
    source_path: src/join.sol
    contract_name: GemJoin
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
- id: pot-ethereum
  contract_id: pot
  contract_name: Pot
  status: live
  chain: Ethereum
  address: '0x197E90f9FAD81970bA7976f33CbD77088E5D7cf7'
  implementation:
    codebase: dss-v1-2
    submodule_path: "./branch-v1.2"
    source_path: src/pot.sol
    contract_name: Pot
    compiler:
      version: 0.5.12
      optimized: false
      evm_version: default
- id: dog-ethereum
  contract_id: dog
  contract_name: Dog
  status: live
  chain: Ethereum
  address: '0x135954d155898D42C90D2a57824C690e0c7BEf1B'
  implementation:
    codebase: dss-master
    submodule_path: "./branch-master"
    source_path: src/dog.sol
    contract_name: Dog
    compiler:
      version: 0.6.12
      optimized: false
      evm_version: default
- id: clipper-ethereum
  contract_id: clipper
  contract_name: Clipper
  status: live
  chain: Ethereum
  address: '0xc67963a226eddd77B91aD8c421630A1b0AdFF270'
  implementation:
    codebase: dss-master
    submodule_path: "./branch-master"
    source_path: src/clip.sol
    contract_name: Clipper
    compiler:
      version: 0.6.12
      optimized: false
      evm_version: default
- id: stairstep-exponential-decrease-ethereum
  contract_id: stairstep-exponential-decrease
  contract_name: StairstepExponentialDecrease
  status: live
  chain: Ethereum
  address: '0x7d9f92DAa9254Bbd1f479DBE5058f74C2381A898'
  implementation:
    codebase: dss-master
    submodule_path: "./branch-master"
    source_path: src/abaci.sol
    contract_name: StairstepExponentialDecrease
    compiler:
      version: 0.6.12
      optimized: false
      evm_version: default
deployment_gaps:
- contract_id: linear-decrease
  contract_name: LinearDecrease
  implementation:
    codebase: dss-master
    submodule_path: "./branch-master"
    source_path: src/abaci.sol
    contract_name: LinearDecrease
    compiler:
      version: 0.6.12
      optimized: false
      evm_version: default
- contract_id: exponential-decrease
  contract_name: ExponentialDecrease
  implementation:
    codebase: dss-master
    submodule_path: "./branch-master"
    source_path: src/abaci.sol
    contract_name: ExponentialDecrease
    compiler:
      version: 0.6.12
      optimized: false
      evm_version: default
```

## Audit Reports

```yaml
audit_reports:
- id: trail-of-bits-mcd
  auditor: Trail of Bits
  report_title: MakerDAO Multi-Collateral Dai Final Report
  current_version: final
  versions:
  - id: final
    reference_refs:
    - trail-of-bits-mcd-final
    version_label: Final
    status: current
    audited_codebases:
    - dss-v1-2
    audited_sources:
    - codebase: dss-v1-2
      path: src/dai.sol
    - codebase: dss-v1-2
      path: src/join.sol
    - codebase: dss-v1-2
      path: src/jug.sol
    - codebase: dss-v1-2
      path: src/pot.sol
    - codebase: dss-v1-2
      path: src/spot.sol
    - codebase: dss-v1-2
      path: src/vat.sol
    - codebase: dss-v1-2
      path: src/vow.sol
    covered_contracts:
    - id: dai
      name: Dai
    - id: dai-join
      name: DaiJoin
    - id: gem-join
      name: GemJoin
    - id: jug
      name: Jug
    - id: pot
      name: Pot
    - id: spotter
      name: Spotter
    - id: vat
      name: Vat
    - id: vow
      name: Vow
    scope_notes: Multi-Collateral Dai launch audit mapped to the dss module.
- id: peckshield-mcd
  auditor: PeckShield
  report_title: MakerDAO Multi-Collateral Dai Final Audit Report
  current_version: final
  versions:
  - id: final
    reference_refs:
    - peckshield-mcd-final
    version_label: Final
    status: current
    audited_codebases:
    - dss-v1-2
    audited_sources:
    - codebase: dss-v1-2
      path: src/dai.sol
    - codebase: dss-v1-2
      path: src/join.sol
    - codebase: dss-v1-2
      path: src/jug.sol
    - codebase: dss-v1-2
      path: src/pot.sol
    - codebase: dss-v1-2
      path: src/spot.sol
    - codebase: dss-v1-2
      path: src/vat.sol
    - codebase: dss-v1-2
      path: src/vow.sol
    covered_contracts:
    - id: dai
      name: Dai
    - id: dai-join
      name: DaiJoin
    - id: gem-join
      name: GemJoin
    - id: jug
      name: Jug
    - id: pot
      name: Pot
    - id: spotter
      name: Spotter
    - id: vat
      name: Vat
    - id: vow
      name: Vow
    scope_notes: Multi-Collateral Dai launch audit mapped to the dss module.
references:
- id: trail-of-bits-mcd-final
  type: audit_report
  title: Trail of Bits MakerDAO Multi-Collateral Dai Final Report
  url: https://raw.githubusercontent.com/sky-ecosystem/mcd-security/master/Audit%20Reports/TOB_MakerDAO_Final_Report.pdf
  path: audit-reports/trail-of-bits-mcd-final.pdf
  date_checked: '2026-06-08'
  content_sha256: c8bbd2a107626ec96d4f61c663beb9be85c86eadc85c82debcefc2a7f0dfa458
- id: peckshield-mcd-final
  type: audit_report
  title: PeckShield MakerDAO Multi-Collateral Dai Final Audit Report
  url: https://raw.githubusercontent.com/sky-ecosystem/mcd-security/master/Audit%20Reports/PeckShield_Final_Audit_Report.pdf
  path: audit-reports/peckshield-mcd-final.pdf
  date_checked: '2026-06-08'
  content_sha256: 8bd75c722b52ed9eb0fdabae96f134fcf388d4cdca75c08d2e5b8b22bd39ed90
```

## Notes

`LinearDecrease` and `ExponentialDecrease` have no deployed address in `info.yaml`. The contracts-list crosswalk selects the active `MCD_CLIP_CALC_ETH_A` row for the deployed abacus instance present in module info.
