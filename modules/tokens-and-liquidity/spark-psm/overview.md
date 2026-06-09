# spark-psm

## Codebases

```yaml
repositories:
- id: spark-psm
  name: spark-psm
  provider: github
  url: https://github.com/sparkdotfi/spark-psm
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./branch-master"
    checked_out_branch: master
    pinned_commit: 2b1a72a7c24f95db0c4bda13ea9062ce9824577b
```

## Deployments

```yaml
deployments: []
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-spark-psm
  auditor: ChainSecurity
  report_title: Spark PSM Audit
  current_version: v2024-10
  versions:
  - id: v2024-10
    reference_refs:
    - chainsecurity-spark-psm-2024-10
    version_label: October 2024
    status: current
    audited_codebases:
    - spark-psm
    audited_sources:
    - codebase: spark-psm
      path: src/PSM3.sol
    covered_contracts:
    - id: psm3
      name: PSM3
- id: cantina-spark-psm
  auditor: Cantina
  report_title: Spark PSM Audit
  current_version: v2024-10
  versions:
  - id: v2024-09
    reference_refs:
    - cantina-spark-psm-2024-09
    version_label: September 2024
    status: superseded
    superseded_by: v2024-10
    audited_codebases:
    - spark-psm
    audited_sources:
    - codebase: spark-psm
      path: src/PSM3.sol
    covered_contracts:
    - id: psm3
      name: PSM3
  - id: v2024-10
    reference_refs:
    - cantina-spark-psm-2024-10
    version_label: October 2024
    status: current
    supersedes:
    - v2024-09
    audited_codebases:
    - spark-psm
    audited_sources:
    - codebase: spark-psm
      path: src/PSM3.sol
    covered_contracts:
    - id: psm3
      name: PSM3
references:
- id: chainsecurity-spark-psm-2024-10
  type: audit_report
  title: ChainSecurity Spark PSM Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-psm/master/audits/20241022-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-spark-psm-2024-10.pdf
  date_published: '2024-10-22'
  date_checked: '2026-06-08'
  content_sha256: 05e18d3134b3838c172815b73e60a47075059acd4b519772310ea29a02df37e3
- id: cantina-spark-psm-2024-09
  type: audit_report
  title: Cantina Spark PSM Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-psm/master/audits/20240909-cantina-audit.pdf
  path: audit-reports/cantina-spark-psm-2024-09.pdf
  date_published: '2024-09-09'
  date_checked: '2026-06-08'
  content_sha256: c90a715fcc53c6d74fe6d251197538f5d1abdbe4f6e8a8f2de22ee633f61542a
- id: cantina-spark-psm-2024-10
  type: audit_report
  title: Cantina Spark PSM Audit
  url: https://raw.githubusercontent.com/sparkdotfi/spark-psm/master/audits/20241023-cantina-audit.pdf
  path: audit-reports/cantina-spark-psm-2024-10.pdf
  date_published: '2024-10-23'
  date_checked: '2026-06-08'
  content_sha256: ab73ac27483e4ea6e33c6bf3ab72db4f5ab0b6591ae393eb21b06bfd75d91edf
```

## Notes

`PSM3` has a contract/source record but no live deployment record in the source metadata.
