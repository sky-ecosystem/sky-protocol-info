# diamond-pau

## Codebases

```yaml
repositories:
- id: diamond-pau
  name: diamond-pau
  provider: github
  url: https://github.com/sky-ecosystem/diamond-pau
  ref: dev
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/diamond-pau/branch-dev"
    checked_out_branch: dev
    pinned_commit: 215f7be581efc2d6d6dd3303ff8c6b45631e368d
- id: pau-administered-agent
  name: pau-administered-agent
  provider: github
  url: https://github.com/sky-ecosystem/pau-administered-agent
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/pau-administered-agent/branch-master"
    checked_out_branch: master
    pinned_commit: bfaaf709a8664d74d12604455f0365a0a12439cf
```

## Deployments

```yaml
deployments: []
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-diamond-pau-audit
  auditor: ChainSecurity
  report_title: Diamond PAU Audit
  current_version: v1130
  versions:
  - id: v1130
    reference_refs:
    - chainsecurity-diamond-pau-audit-v1130
    version_label: v1130
    status: current
    audited_codebases:
    - diamond-pau
    audited_sources:
    - codebase: diamond-pau
      path: src/ALMProxy.sol
    - codebase: diamond-pau
      path: src/ALMProxyFreezable.sol
    - codebase: diamond-pau
      path: src/AccessControls.sol
    - codebase: diamond-pau
      path: src/Beacon.sol
    - codebase: diamond-pau
      path: src/Controller.sol
    - codebase: diamond-pau
      path: src/PAUFactory.sol
    - codebase: diamond-pau
      path: src/RateLimits.sol
    covered_contracts:
    - id: alm-proxy
      name: ALMProxy
    - id: alm-proxy-freezable
      name: ALMProxyFreezable
    - id: access-controls
      name: AccessControls
    - id: beacon
      name: Beacon
    - id: controller
      name: Controller
    - id: pau-factory
      name: PAUFactory
    - id: rate-limits
      name: RateLimits
- id: cantina-diamond-pau-audit
  auditor: Cantina
  report_title: Diamond PAU Audit
  current_version: v1130
  versions:
  - id: v1130
    reference_refs:
    - cantina-diamond-pau-audit-v1130
    version_label: v1130
    status: current
    audited_codebases:
    - diamond-pau
    audited_sources:
    - codebase: diamond-pau
      path: src/ALMProxy.sol
    - codebase: diamond-pau
      path: src/ALMProxyFreezable.sol
    - codebase: diamond-pau
      path: src/AccessControls.sol
    - codebase: diamond-pau
      path: src/Beacon.sol
    - codebase: diamond-pau
      path: src/Controller.sol
    - codebase: diamond-pau
      path: src/PAUFactory.sol
    - codebase: diamond-pau
      path: src/RateLimits.sol
    covered_contracts:
    - id: alm-proxy
      name: ALMProxy
    - id: alm-proxy-freezable
      name: ALMProxyFreezable
    - id: access-controls
      name: AccessControls
    - id: beacon
      name: Beacon
    - id: controller
      name: Controller
    - id: pau-factory
      name: PAUFactory
    - id: rate-limits
      name: RateLimits
- id: certora-diamond-pau-audit
  auditor: Certora
  report_title: Diamond PAU Audit
  current_version: v1120
  versions:
  - id: v1120
    reference_refs:
    - certora-diamond-pau-audit-v1120
    version_label: v1120
    status: current
    audited_codebases:
    - diamond-pau
    audited_sources:
    - codebase: diamond-pau
      path: src/ALMProxy.sol
    - codebase: diamond-pau
      path: src/ALMProxyFreezable.sol
    - codebase: diamond-pau
      path: src/AccessControls.sol
    - codebase: diamond-pau
      path: src/Beacon.sol
    - codebase: diamond-pau
      path: src/Controller.sol
    - codebase: diamond-pau
      path: src/PAUFactory.sol
    - codebase: diamond-pau
      path: src/RateLimits.sol
    covered_contracts:
    - id: alm-proxy
      name: ALMProxy
    - id: alm-proxy-freezable
      name: ALMProxyFreezable
    - id: access-controls
      name: AccessControls
    - id: beacon
      name: Beacon
    - id: controller
      name: Controller
    - id: pau-factory
      name: PAUFactory
    - id: rate-limits
      name: RateLimits
- id: octane-diamond-pau-audit
  auditor: Octane
  report_title: Diamond PAU Audit
  current_version: v1120
  versions:
  - id: v1120
    reference_refs:
    - octane-diamond-pau-audit-v1120
    version_label: v1120
    status: current
    audited_codebases:
    - diamond-pau
    audited_sources:
    - codebase: diamond-pau
      path: src/ALMProxy.sol
    - codebase: diamond-pau
      path: src/ALMProxyFreezable.sol
    - codebase: diamond-pau
      path: src/AccessControls.sol
    - codebase: diamond-pau
      path: src/Beacon.sol
    - codebase: diamond-pau
      path: src/Controller.sol
    - codebase: diamond-pau
      path: src/PAUFactory.sol
    - codebase: diamond-pau
      path: src/RateLimits.sol
    covered_contracts:
    - id: alm-proxy
      name: ALMProxy
    - id: alm-proxy-freezable
      name: ALMProxyFreezable
    - id: access-controls
      name: AccessControls
    - id: beacon
      name: Beacon
    - id: controller
      name: Controller
    - id: pau-factory
      name: PAUFactory
    - id: rate-limits
      name: RateLimits
- id: unvariant-diamond-pau-audit
  auditor: Unvariant
  report_title: Diamond PAU Audit
  current_version: v1120
  versions:
  - id: v1120
    reference_refs:
    - unvariant-diamond-pau-audit-v1120
    version_label: v1120
    status: current
    audited_codebases:
    - diamond-pau
    audited_sources:
    - codebase: diamond-pau
      path: src/ALMProxy.sol
    - codebase: diamond-pau
      path: src/ALMProxyFreezable.sol
    - codebase: diamond-pau
      path: src/AccessControls.sol
    - codebase: diamond-pau
      path: src/Beacon.sol
    - codebase: diamond-pau
      path: src/Controller.sol
    - codebase: diamond-pau
      path: src/PAUFactory.sol
    - codebase: diamond-pau
      path: src/RateLimits.sol
    covered_contracts:
    - id: alm-proxy
      name: ALMProxy
    - id: alm-proxy-freezable
      name: ALMProxyFreezable
    - id: access-controls
      name: AccessControls
    - id: beacon
      name: Beacon
    - id: controller
      name: Controller
    - id: pau-factory
      name: PAUFactory
    - id: rate-limits
      name: RateLimits
references:
- id: chainsecurity-diamond-pau-audit-v1130
  type: audit_report
  title: ChainSecurity Diamond PAU Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/diamond-pau/215f7be581efc2d6d6dd3303ff8c6b45631e368d/audits/v1130-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-diamond-pau-audit-v1130.pdf
  date_checked: '2026-06-09'
  content_sha256: 8a19c85ca8e3eb39030a51a7a42ecfce6f8d1e339194759a06bc7f35651ba5ab
- id: cantina-diamond-pau-audit-v1130
  type: audit_report
  title: Cantina Diamond PAU Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/diamond-pau/215f7be581efc2d6d6dd3303ff8c6b45631e368d/audits/v1130-cantina-audit.pdf
  path: audit-reports/cantina-diamond-pau-audit-v1130.pdf
  date_checked: '2026-06-09'
  content_sha256: 6ee19baa8e74cefdbde26df5c93089e33cf16ca175a817339cbe7af048de47c7
- id: certora-diamond-pau-audit-v1120
  type: audit_report
  title: Certora Diamond PAU Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/diamond-pau/215f7be581efc2d6d6dd3303ff8c6b45631e368d/audits/v1120-certora-audit.pdf
  path: audit-reports/certora-diamond-pau-audit-v1120.pdf
  date_checked: '2026-06-09'
  content_sha256: 0c68d29891a97fe94c5eff8fe670c71865f57e65b3c3c0a1d7314ba1a87f702a
- id: octane-diamond-pau-audit-v1120
  type: audit_report
  title: Octane Diamond PAU Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/diamond-pau/215f7be581efc2d6d6dd3303ff8c6b45631e368d/audits/v1120-octane-audit.pdf
  path: audit-reports/octane-diamond-pau-audit-v1120.pdf
  date_checked: '2026-06-09'
  content_sha256: a8986c9b96bd71f941cd92ad2a5c13ad0f4b444f4c0d98c2bd94dc6476ecb161
- id: unvariant-diamond-pau-audit-v1120
  type: audit_report
  title: Unvariant Diamond PAU Audit
  url: https://raw.githubusercontent.com/sky-ecosystem/diamond-pau/215f7be581efc2d6d6dd3303ff8c6b45631e368d/audits/v1120-unvariant_audit.pdf
  path: audit-reports/unvariant-diamond-pau-audit-v1120.pdf
  date_checked: '2026-06-09'
  content_sha256: 7d6b8d635bd887f924313f1995c304b4c4093ebec57428bb907ccc0e54aec402
```

## Notes

```yaml
notes:
- No deployed addresses are recorded for this module.
- No audit reports were found in the pau-administered-agent repository at the pinned commit.
```
