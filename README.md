# Sky Protocol

Tracks public records for Sky Protocol modules.

Each module record links the source code, deployment addresses, audit reports,
and notes for one protocol component.

## Module Records

- source codebase URLs, refs, and pinned commits
- git submodules for the source commits used by the record
- deployed contract addresses and implementation source paths
- audit report metadata, public report URLs, and local PDF copies

`overview.md` is the entry point for each module.

## Repository Layout

```text
modules/<group>/<module>/
  overview.md          # codebases, deployments, audit reports, and notes
  audit-reports/       # local copies of referenced audit PDFs
  <source-submodule>/  # pinned source repository checkout
```

## Licenses

[`LICENSES`](LICENSES) lists each module's license term and the copyright
notices found in that module's primary contract files.
