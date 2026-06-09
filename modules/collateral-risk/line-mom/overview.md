# line-mom

## Codebases

```yaml
repositories:
- id: line-mom
  name: line-mom
  provider: github
  url: https://github.com/sky-ecosystem/line-mom
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: 5935e56ac8d4d677865259e94129bf2bd3039ebf
```

## Deployments

```yaml
deployments:
- id: line-mom-ethereum
  contract_id: line-mom
  contract_name: LineMom
  status: live
  chain: Ethereum
  address: '0x9c257e5Aaf73d964aEBc2140CA38078988fB0C10'
  implementation:
    codebase: line-mom
    submodule_path: "./branch-master"
    source_path: src/LineMom.sol
    contract_name: LineMom
    compiler:
      version: 0.8.16
      optimized: false
      evm_version: default
```

## Audit Reports

```yaml
audit_reports: []
```
