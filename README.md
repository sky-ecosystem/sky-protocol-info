# Sky Protocol

Tracks public records for Sky Protocol modules.

## Modules

### Capital Allocation

- [diamond-pau](modules/capital-allocation/diamond-pau/)
- [dss-allocator](modules/capital-allocation/dss-allocator/)

### Chain Bridges

- [arbitrum-dai-bridge](modules/chain-bridges/arbitrum-dai-bridge/)
- [arbitrum-token-bridge](modules/chain-bridges/arbitrum-token-bridge/)
- [lz-governance-relay](modules/chain-bridges/lz-governance-relay/)
- [op-token-bridge](modules/chain-bridges/op-token-bridge/)
- [optimism-dai-bridge](modules/chain-bridges/optimism-dai-bridge/)
- [sky-oapp-oft](modules/chain-bridges/sky-oapp-oft/)

### Collateral Risk

- [clipper-mom](modules/collateral-risk/clipper-mom/)
- [dss-auto-line](modules/collateral-risk/dss-auto-line/)
- [line-mom](modules/collateral-risk/line-mom/)
- [osm](modules/collateral-risk/osm/)
- [sp-beam](modules/collateral-risk/sp-beam/)

### Core System

- [dss](modules/core-system/dss/)

### Governance Control

- [chief](modules/governance-control/chief/)
- [ds-pause](modules/governance-control/ds-pause/)
- [star-guard](modules/governance-control/star-guard/)
- [vote-delegate](modules/governance-control/vote-delegate/)

### Grove

- [grove-basin](modules/grove/grove-basin/)

### Savings and Staking

- [lockstake](modules/savings-and-staking/lockstake/)
- [stusds](modules/savings-and-staking/stusds/)
- [susds](modules/savings-and-staking/susds/)

### Spark

- [spark-alm-controller](modules/spark/spark-alm-controller/)
- [spark-governance](modules/spark/spark-governance/)
- [spark-lend](modules/spark/spark-lend/)
- [spark-rewards](modules/spark/spark-rewards/)
- [spark-savings](modules/spark/spark-savings/)

### Surplus and Rewards

- [dss-flappers](modules/surplus-and-rewards/dss-flappers/)
- [dss-vest](modules/surplus-and-rewards/dss-vest/)
- [endgame-toolkit](modules/surplus-and-rewards/endgame-toolkit/)

### Tokens and Liquidity

- [dss-flash](modules/tokens-and-liquidity/dss-flash/)
- [dss-lite-psm](modules/tokens-and-liquidity/dss-lite-psm/)
- [sky](modules/tokens-and-liquidity/sky/)
- [usds](modules/tokens-and-liquidity/usds/)

## Repository Structure

Each module record links the source code, deployment addresses, audit reports,
and notes for one protocol component.

- source codebase URLs, refs, and pinned commits
- git submodules for the source commits used by the record
- deployed contract addresses and implementation source paths
- audit report metadata, public report URLs, and local PDF copies

`overview.md` is the entry point for each module.

```text
modules/<group>/<module>/
  overview.md          # codebases, deployments, audit reports, and notes
  audit-reports/       # local copies of referenced audit PDFs
  codebases/
    <codebase>/
      <checkout>/      # branch-* or commit-* pinned source checkout
```

## Licenses

[`LICENSES`](LICENSES) lists each module's license term and the copyright
notices found in that module's primary contract files.
