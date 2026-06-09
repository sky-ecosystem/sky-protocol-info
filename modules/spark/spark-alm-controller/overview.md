# spark-alm-controller

## Codebases

```yaml
repositories:
- id: spark-alm-controller
  name: spark-alm-controller
  provider: github
  url: https://github.com/sparkdotfi/spark-alm-controller
  ref: dev
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    checked_out_branch: dev
    pinned_commit: 0fee4b5b1bc4de7da1e7aa5b91a98375ef6849a2
```

## Deployments

```yaml
deployments:
- id: alm-controller-ethereum
  contract_id: alm-controller
  contract_name: MainnetController
  status: live
  chain: Ethereum
  address: '0x5c46Fc65855c0C7465a1EA85EEA0B24B601502D3'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/MainnetController.sol
    contract_name: MainnetController
- id: alm-proxy-ethereum
  contract_id: alm-proxy
  contract_name: ALMProxy
  status: live
  chain: Ethereum
  address: '0x1601843c5E9bC251A3272907010AFa41Fa18347E'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ALMProxy.sol
    contract_name: ALMProxy
- id: alm-proxy-freezable-ethereum
  contract_id: alm-proxy-freezable
  contract_name: ALMProxyFreezable
  status: live
  chain: Ethereum
  address: '0x9Ad87668d49ab69EEa0AF091de970EF52b0D5178'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ALMProxyFreezable.sol
    contract_name: ALMProxyFreezable
- id: alm-rate-limits-ethereum
  contract_id: alm-rate-limits
  contract_name: RateLimits
  status: live
  chain: Ethereum
  address: '0x7A5FD5cf045e010e62147F065cEAe59e5344b188'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/RateLimits.sol
    contract_name: RateLimits
- id: alm-controller-base
  contract_id: alm-controller
  contract_name: ForeignController
  status: live
  chain: Base
  address: '0x86036CE5d2f792367C0AA43164e688d13c5A60A8'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ForeignController.sol
    contract_name: ForeignController
- id: alm-proxy-base
  contract_id: alm-proxy
  contract_name: ALMProxy
  status: live
  chain: Base
  address: '0x2917956eFF0B5eaF030abDB4EF4296DF775009cA'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ALMProxy.sol
    contract_name: ALMProxy
- id: alm-proxy-freezable-base
  contract_id: alm-proxy-freezable
  contract_name: ALMProxyFreezable
  status: live
  chain: Base
  address: '0xCBA0C0a2a0B6Bb11233ec4EA85C5bFfea33e724d'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ALMProxyFreezable.sol
    contract_name: ALMProxyFreezable
- id: alm-rate-limits-base
  contract_id: alm-rate-limits
  contract_name: RateLimits
  status: live
  chain: Base
  address: '0x983eC82E45C61a42FDDA7B3c43B8C767004c8A74'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/RateLimits.sol
    contract_name: RateLimits
- id: alm-controller-arbitrum-one
  contract_id: alm-controller
  contract_name: ForeignController
  status: live
  chain: Arbitrum One
  address: '0xC40611AC4Fff8572Dc5F02A238176edCF15Ea7ba'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ForeignController.sol
    contract_name: ForeignController
- id: alm-proxy-arbitrum-one
  contract_id: alm-proxy
  contract_name: ALMProxy
  status: live
  chain: Arbitrum One
  address: '0x92afd6F2385a90e44da3a8B60fe36f6cBe1D8709'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ALMProxy.sol
    contract_name: ALMProxy
- id: alm-rate-limits-arbitrum-one
  contract_id: alm-rate-limits
  contract_name: RateLimits
  status: live
  chain: Arbitrum One
  address: '0x19D08879851FB54C2dCc4bb32b5a1EA5E9Ad6838'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/RateLimits.sol
    contract_name: RateLimits
- id: alm-controller-optimism
  contract_id: alm-controller
  contract_name: ForeignController
  status: live
  chain: Optimism
  address: '0x689502bc817E6374286af8f171Ed4715721406f7'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ForeignController.sol
    contract_name: ForeignController
- id: alm-proxy-optimism
  contract_id: alm-proxy
  contract_name: ALMProxy
  status: live
  chain: Optimism
  address: '0x876664f0c9Ff24D1aa355Ce9f1680AE1A5bf36fB'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ALMProxy.sol
    contract_name: ALMProxy
- id: alm-rate-limits-optimism
  contract_id: alm-rate-limits
  contract_name: RateLimits
  status: live
  chain: Optimism
  address: '0x6B34A6B84444dC3Fc692821D5d077a1e4927342d'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/RateLimits.sol
    contract_name: RateLimits
- id: alm-controller-unichain
  contract_id: alm-controller
  contract_name: ForeignController
  status: live
  chain: Unichain
  address: '0xF16DE710899C7bdd6D46873265392CCA68e5D5bA'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ForeignController.sol
    contract_name: ForeignController
- id: alm-proxy-unichain
  contract_id: alm-proxy
  contract_name: ALMProxy
  status: live
  chain: Unichain
  address: '0x345E368fcCd62266B3f5F37C9a131FD1c39f5869'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ALMProxy.sol
    contract_name: ALMProxy
- id: alm-rate-limits-unichain
  contract_id: alm-rate-limits
  contract_name: RateLimits
  status: live
  chain: Unichain
  address: '0x5A1a44D2192Dd1e21efB9caA50E32D0716b35535'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/RateLimits.sol
    contract_name: RateLimits
- id: alm-controller-avalanche
  contract_id: alm-controller
  contract_name: ForeignController
  status: live
  chain: Avalanche
  address: '0x4eE67c8Db1BAa6ddE99d936C7D313B5d31e8fa38'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ForeignController.sol
    contract_name: ForeignController
- id: alm-proxy-avalanche
  contract_id: alm-proxy
  contract_name: ALMProxy
  status: live
  chain: Avalanche
  address: '0xecE6B0E8a54c2f44e066fBb9234e7157B15b7FeC'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ALMProxy.sol
    contract_name: ALMProxy
- id: alm-proxy-freezable-avalanche
  contract_id: alm-proxy-freezable
  contract_name: ALMProxyFreezable
  status: live
  chain: Avalanche
  address: '0x45d91340B3B7B96985A72b5c678F7D9e8D664b62'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/ALMProxyFreezable.sol
    contract_name: ALMProxyFreezable
- id: alm-rate-limits-avalanche
  contract_id: alm-rate-limits
  contract_name: RateLimits
  status: live
  chain: Avalanche
  address: '0xb79972e8B21f0dE911E65AC342ac85ad38C9A77a'
  implementation:
    codebase: spark-alm-controller
    submodule_path: "./codebases/spark-alm-controller/branch-dev"
    source_path: src/RateLimits.sol
    contract_name: RateLimits
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-spark-alm-controller-audit
  auditor: ChainSecurity
  report_title: Spark ALM Controller Audit
  current_version: v1100
  versions:
  - id: v1100
    reference_refs:
    - chainsecurity-spark-alm-controller-audit-v1100
    version_label: v1100
    status: current
    audited_codebases:
    - spark-alm-controller
    audited_sources:
    - codebase: spark-alm-controller
      path: src/ALMProxy.sol
    - codebase: spark-alm-controller
      path: src/ALMProxyFreezable.sol
    - codebase: spark-alm-controller
      path: src/ForeignController.sol
    - codebase: spark-alm-controller
      path: src/MainnetController.sol
    - codebase: spark-alm-controller
      path: src/RateLimits.sol
    covered_contracts:
    - id: alm-proxy
      name: ALMProxy
    - id: alm-proxy-freezable
      name: ALMProxyFreezable
    - id: foreign-controller
      name: ForeignController
    - id: mainnet-controller
      name: MainnetController
    - id: rate-limits
      name: RateLimits
- id: cantina-spark-alm-controller-audit
  auditor: Cantina
  report_title: Spark ALM Controller Audit
  current_version: v1100
  versions:
  - id: v1100
    reference_refs:
    - cantina-spark-alm-controller-audit-v1100
    version_label: v1100
    status: current
    audited_codebases:
    - spark-alm-controller
    audited_sources:
    - codebase: spark-alm-controller
      path: src/ALMProxy.sol
    - codebase: spark-alm-controller
      path: src/ALMProxyFreezable.sol
    - codebase: spark-alm-controller
      path: src/ForeignController.sol
    - codebase: spark-alm-controller
      path: src/MainnetController.sol
    - codebase: spark-alm-controller
      path: src/RateLimits.sol
    covered_contracts:
    - id: alm-proxy
      name: ALMProxy
    - id: alm-proxy-freezable
      name: ALMProxyFreezable
    - id: foreign-controller
      name: ForeignController
    - id: mainnet-controller
      name: MainnetController
    - id: rate-limits
      name: RateLimits
- id: certora-spark-alm-controller-audit
  auditor: Certora
  report_title: Spark ALM Controller Audit
  current_version: v190
  versions:
  - id: v190
    reference_refs:
    - certora-spark-alm-controller-audit-v190
    version_label: v190
    status: current
    audited_codebases:
    - spark-alm-controller
    audited_sources:
    - codebase: spark-alm-controller
      path: src/ALMProxy.sol
    - codebase: spark-alm-controller
      path: src/ALMProxyFreezable.sol
    - codebase: spark-alm-controller
      path: src/ForeignController.sol
    - codebase: spark-alm-controller
      path: src/MainnetController.sol
    - codebase: spark-alm-controller
      path: src/RateLimits.sol
    covered_contracts:
    - id: alm-proxy
      name: ALMProxy
    - id: alm-proxy-freezable
      name: ALMProxyFreezable
    - id: foreign-controller
      name: ForeignController
    - id: mainnet-controller
      name: MainnetController
    - id: rate-limits
      name: RateLimits
references:
- id: chainsecurity-spark-alm-controller-audit-v1100
  type: audit_report
  title: ChainSecurity Spark ALM Controller Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-alm-controller/0fee4b5b1bc4de7da1e7aa5b91a98375ef6849a2/audits/v1100-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-spark-alm-controller-audit-v1100.pdf
  date_checked: '2026-06-09'
  content_sha256: 90695d04231c62a057be5b96f5e92a675235a85deb53ded6aff983c841f364ca
- id: cantina-spark-alm-controller-audit-v1100
  type: audit_report
  title: Cantina Spark ALM Controller Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-alm-controller/0fee4b5b1bc4de7da1e7aa5b91a98375ef6849a2/audits/v1100-cantina-audit.pdf
  path: audit-reports/cantina-spark-alm-controller-audit-v1100.pdf
  date_checked: '2026-06-09'
  content_sha256: 9b4ebb55888ba88d4e64336556d3f6659f8fbd2b40e79deb741b3b69b6fd3184
- id: certora-spark-alm-controller-audit-v190
  type: audit_report
  title: Certora Spark ALM Controller Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-alm-controller/0fee4b5b1bc4de7da1e7aa5b91a98375ef6849a2/audits/v190-certora-audit.pdf
  path: audit-reports/certora-spark-alm-controller-audit-v190.pdf
  date_checked: '2026-06-09'
  content_sha256: 0c3a0086345253cc117709b826c336865b46f6aa068c608436dad6ad40afe961
```

## Notes
