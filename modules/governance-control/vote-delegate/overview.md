# vote-delegate

## Codebases

```yaml
repositories:
- id: vote-delegate
  name: vote-delegate
  provider: github
  url: https://github.com/sky-ecosystem/vote-delegate
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/vote-delegate/branch-master"
    checked_out_branch: master
    pinned_commit: 6d9359e58a452c28425121900a3b1b4ca3317ead
```

## Deployments

```yaml
deployments:
- id: vote-delegate-ethereum
  contract_id: vote-delegate
  contract_name: VoteDelegate
  status: live
  chain: Ethereum
  address: '0xd112008aa18607Ec1401ff9c7f1943B460628553'
  implementation:
    codebase: vote-delegate
    submodule_path: "./codebases/vote-delegate/branch-master"
    source_path: src/VoteDelegate.sol
    contract_name: VoteDelegate
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
- id: vote-delegate-factory-ethereum
  contract_id: vote-delegate-factory
  contract_name: VoteDelegateFactory
  status: live
  chain: Ethereum
  address: '0x4Cf3DaeFA2683Cd18df00f7AFF5169C00a9EccD5'
  implementation:
    codebase: vote-delegate
    submodule_path: "./codebases/vote-delegate/branch-master"
    source_path: src/VoteDelegateFactory.sol
    contract_name: VoteDelegateFactory
    compiler:
      version: 0.8.21
      optimized: true
      runs: 200
      evm_version: shanghai
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-vote-delegate
  auditor: ChainSecurity
  report_title: Sky VoteDelegate Audit
  current_version: v2025-04
  versions:
  - id: v2025-04
    reference_refs:
    - chainsecurity-vote-delegate-2025-04
    version_label: April 2025
    status: current
    audited_codebases:
    - vote-delegate
    audited_sources:
    - codebase: vote-delegate
      path: src/VoteDelegate.sol
    - codebase: vote-delegate
      path: src/VoteDelegateFactory.sol
    covered_contracts:
    - id: vote-delegate
      name: VoteDelegate
    - id: vote-delegate-factory
      name: VoteDelegateFactory
- id: cantina-vote-delegate
  auditor: Cantina
  report_title: Sky Vote Delegate Updates Audit
  current_version: v2025-04
  versions:
  - id: v2025-04
    reference_refs:
    - cantina-vote-delegate-2025-04
    version_label: April 2025
    status: current
    audited_codebases:
    - vote-delegate
    audited_sources:
    - codebase: vote-delegate
      path: src/VoteDelegate.sol
    - codebase: vote-delegate
      path: src/VoteDelegateFactory.sol
    covered_contracts:
    - id: vote-delegate
      name: VoteDelegate
    - id: vote-delegate-factory
      name: VoteDelegateFactory
references:
- id: chainsecurity-vote-delegate-2025-04
  type: audit_report
  title: ChainSecurity Sky VoteDelegate Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/vote-delegate/master/audit/20250424-ChainSecurity_Sky_VoteDelegate_audit.pdf
  path: audit-reports/chainsecurity-vote-delegate-2025-04.pdf
  date_published: '2025-04-24'
  date_checked: '2026-06-08'
  content_sha256: 60f71387fe34a09b3bfc3a8859bf23776d27ed5d32a136f6a0bd0a424bfacb39
- id: cantina-vote-delegate-2025-04
  type: audit_report
  title: Cantina Sky Vote Delegate Updates Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/vote-delegate/master/audit/20250430-cantina-report-sky-vote-delegate-updates.pdf
  path: audit-reports/cantina-vote-delegate-2025-04.pdf
  date_published: '2025-04-30'
  date_checked: '2026-06-08'
  content_sha256: de155e337f805a3ccdaa54d9ffe724baef708c9c7101d381d2f0c226c75fbcac
```

## Notes

`VoteDelegate` at `0xd112008aa18607Ec1401ff9c7f1943B460628553` has no active contracts-list row. The contracts list tracks the active `VOTE_DELEGATE_FACTORY` row, while this address is a factory-created delegate instance recognized by that factory.
