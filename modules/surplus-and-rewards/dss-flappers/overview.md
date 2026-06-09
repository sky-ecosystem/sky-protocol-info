# dss-flappers

## Codebases

```yaml
repositories:
- id: dss-flappers
  name: dss-flappers
  provider: github
  url: https://github.com/sky-ecosystem/dss-flappers
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/dss-flappers/branch-master"
    checked_out_branch: master
    pinned_commit: ed90ec22b9da12f45e99b8dc2da5a9df48807780
```

## Deployments

```yaml
deployments:
- id: flapper-uni-v2-swap-only-ethereum
  contract_id: flapper-uni-v2-swap-only
  contract_name: FlapperUniV2SwapOnly
  status: live
  chain: Ethereum
  address: '0x374D9c3d5134052Bc558F432Afa1df6575f07407'
  implementation:
    codebase: dss-flappers
    submodule_path: "./codebases/dss-flappers/branch-master"
    source_path: src/FlapperUniV2SwapOnly.sol
    contract_name: FlapperUniV2SwapOnly
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
- id: kicker-ethereum
  contract_id: kicker
  contract_name: Kicker
  status: live
  chain: Ethereum
  address: '0xD889477102e8C4A857b78Fcc2f134535176Ec1Fc'
  implementation:
    codebase: dss-flappers
    submodule_path: "./codebases/dss-flappers/branch-master"
    source_path: src/Kicker.sol
    contract_name: Kicker
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
- id: splitter-ethereum
  contract_id: splitter
  contract_name: Splitter
  status: live
  chain: Ethereum
  address: '0xBF7111F13386d23cb2Fba5A538107A73f6872bCF'
  implementation:
    codebase: dss-flappers
    submodule_path: "./codebases/dss-flappers/branch-master"
    source_path: src/Splitter.sol
    contract_name: Splitter
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
- id: splitter-mom-ethereum
  contract_id: splitter-mom
  contract_name: SplitterMom
  status: live
  chain: Ethereum
  address: '0xF51a075d468dE7dE3599C1Dc47F5C42d02C9230e'
  implementation:
    codebase: dss-flappers
    submodule_path: "./codebases/dss-flappers/branch-master"
    source_path: src/SplitterMom.sol
    contract_name: SplitterMom
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: paris
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-dss-flappers
  auditor: ChainSecurity
  report_title: Sky Dss Flappers Audit
  current_version: v2025-10
  versions:
  - id: v2025-10
    reference_refs:
    - chainsecurity-dss-flappers-2025-10
    version_label: October 2025
    status: current
    audited_codebases:
    - dss-flappers
    audited_sources:
    - codebase: dss-flappers
      path: src/FlapperUniV2SwapOnly.sol
    - codebase: dss-flappers
      path: src/Kicker.sol
    - codebase: dss-flappers
      path: src/Splitter.sol
    - codebase: dss-flappers
      path: src/SplitterMom.sol
    covered_contracts:
    - id: flapper-uni-v2-swap-only
      name: FlapperUniV2SwapOnly
    - id: kicker
      name: Kicker
    - id: splitter
      name: Splitter
    - id: splitter-mom
      name: SplitterMom
- id: cantina-dss-flappers
  auditor: Cantina
  report_title: Sky Flappers Audit
  current_version: v2025-10
  versions:
  - id: v2025-10
    reference_refs:
    - cantina-dss-flappers-2025-10
    version_label: October 2025
    status: current
    audited_codebases:
    - dss-flappers
    audited_sources:
    - codebase: dss-flappers
      path: src/FlapperUniV2SwapOnly.sol
    - codebase: dss-flappers
      path: src/Kicker.sol
    - codebase: dss-flappers
      path: src/Splitter.sol
    - codebase: dss-flappers
      path: src/SplitterMom.sol
    covered_contracts:
    - id: flapper-uni-v2-swap-only
      name: FlapperUniV2SwapOnly
    - id: kicker
      name: Kicker
    - id: splitter
      name: Splitter
    - id: splitter-mom
      name: SplitterMom
references:
- id: chainsecurity-dss-flappers-2025-10
  type: audit_report
  title: ChainSecurity Sky Dss Flappers Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-flappers/master/audit/20251021-ChainSecurity_Sky_Dss_Flappers_audit.pdf
  path: audit-reports/chainsecurity-dss-flappers-2025-10.pdf
  date_published: '2025-10-21'
  date_checked: '2026-06-08'
  content_sha256: e951900ccab6211f529fee89622e729877df35f9d8c70fa99124dc1e2e04f36a
- id: cantina-dss-flappers-2025-10
  type: audit_report
  title: Cantina Sky Flappers Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/dss-flappers/master/audit/20251023-cantina-report-sky-flappers.pdf
  path: audit-reports/cantina-dss-flappers-2025-10.pdf
  date_published: '2025-10-23'
  date_checked: '2026-06-08'
  content_sha256: 9e37726879fea469f2918f46be5b21548a44ac59776d5531557a51d55c1847b2
```
