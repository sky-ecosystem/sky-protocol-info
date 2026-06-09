# osm

## Codebases

```yaml
repositories:
- id: osm
  name: osm
  provider: github
  url: https://github.com/sky-ecosystem/osm
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: e36c874b4e14fba860e48c0cf99cd600c0c59efa
```

## Deployments

```yaml
deployments:
- id: osm-ethereum
  contract_id: osm
  contract_name: OSM
  status: live
  chain: Ethereum
  address: '0x81FE72B5A8d1A857d176C3E7d5Bd2679A9B85763'
  implementation:
    codebase: osm
    submodule_path: "./branch-master"
    source_path: src/osm.sol
    contract_name: OSM
    compiler:
      version: 0.5.12
      optimized: true
      runs: 200
      evm_version: default
```

## Audit Reports

```yaml
audit_reports: []
```
