# dss-flash

## Codebases

```yaml
repositories:
- id: dss-flash
  name: dss-flash
  provider: github
  url: https://github.com/sky-ecosystem/dss-flash
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: 9d492aa6148c35f568400a1ab85cd6df43b2ccc8
```

## Deployments

```yaml
deployments:
- id: dss-flash-ethereum
  contract_id: dss-flash
  contract_name: DssFlash
  status: live
  chain: Ethereum
  address: '0x60744434d6339a6B27d73d9Eda62b6F66a0a04FA'
  implementation:
    codebase: dss-flash
    submodule_path: "./branch-master"
    source_path: src/flash.sol
    contract_name: DssFlash
    compiler:
      version: 0.6.12
      optimized: false
      evm_version: default
```

## Audit Reports

```yaml
audit_reports: []
```
