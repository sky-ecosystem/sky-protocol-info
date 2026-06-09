# dss-auto-line

## Codebases

```yaml
repositories:
- id: dss-auto-line
  name: dss-auto-line
  provider: github
  url: https://github.com/sky-ecosystem/dss-auto-line
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: bff7e6cc43dbd7d9a054dd359ef18a1b4d06b6f5
```

## Deployments

```yaml
deployments:
- id: dss-auto-line-ethereum
  contract_id: dss-auto-line
  contract_name: DssAutoLine
  status: live
  chain: Ethereum
  address: '0xC7Bdd1F2B16447dcf3dE045C4a039A60EC2f0ba3'
  implementation:
    codebase: dss-auto-line
    submodule_path: "./branch-master"
    source_path: src/DssAutoLine.sol
    contract_name: DssAutoLine
    compiler:
      version: 0.6.11
      optimized: true
      runs: 1000000
      evm_version: default
```

## Audit Reports

```yaml
audit_reports: []
```
