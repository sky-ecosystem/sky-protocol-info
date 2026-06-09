# clipper-mom

## Codebases

```yaml
repositories:
- id: clipper-mom
  name: clipper-mom
  provider: github
  url: https://github.com/sky-ecosystem/clipper-mom
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/clipper-mom/branch-master"
    checked_out_branch: master
    pinned_commit: 1473b448cc9141fb0c56146f8b5b28db57b39739
```

## Deployments

```yaml
deployments:
- id: clipper-mom-ethereum
  contract_id: clipper-mom
  contract_name: ClipperMom
  status: live
  chain: Ethereum
  address: '0x79FBDF16b366DFb14F66cE4Ac2815Ca7296405A0'
  implementation:
    codebase: clipper-mom
    submodule_path: "./codebases/clipper-mom/branch-master"
    source_path: src/ClipperMom.sol
    contract_name: ClipperMom
    compiler:
      version: 0.6.12
      optimized: false
      evm_version: default
```

## Audit Reports

```yaml
audit_reports: []
```
