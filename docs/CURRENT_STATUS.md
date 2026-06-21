# Current Status

Last verified: 2026-06-22

This document is a historical snapshot and handoff aid. It is not the live authority for
repository, pull request, or gate state.

```yaml
status_authority:
  live_repository_state: GitHub repository metadata
  live_pr_state: GitHub pull request metadata
  live_gate_state: SHA-bound GitHub PR evidence
  document_role: historical_snapshot_and_handoff
```

Snapshot rules:

- This document must not transcribe `PASS` / `FAIL` results each time a gate result changes.
  Live gate results are read from GitHub PR comments, reviews, checks, and other SHA-bound
  evidence.
- Updating this document must not be used to change the PR head SHA, because doing so would
  invalidate prior verification bound to the previous head SHA.
- In-document state must never be treated as higher authority than GitHub PR metadata. When the
  two differ, GitHub PR metadata governs.

```yaml
project: Pourō-Fable5 Re
phase: governance_foundation
repository:
  full_name: NS-del346/Pouro-Fable5-Re
  exists: true
  visibility: public
  default_branch: main
  initial_commit: 9229c6e6e848fdbf616f36f96cd12410e1c2cf54
  snapshot_main_head_sha: 3211415c66e8461727a5ccfb7e6fddaee9bc20f5
  open_prs_at_last_verified: 0

pr_000a:
  status: merged
  number: 1
  url: https://github.com/NS-del346/Pouro-Fable5-Re/pull/1
  branch: pr-000a-governance-foundation
  base_sha: 9229c6e6e848fdbf616f36f96cd12410e1c2cf54
  head_sha_at_draft_creation: c6c3727801d1049bba0b57673a9cd0b6127dad46
  current_head_sha_authority: GitHub pull request metadata
  merge_performed: true
  merge_commit: f72b3125191119d2dba107069d6a418babde995b

pr_000d:
  status: merged
  number: 2
  merge_performed: true
  merge_commit: a4e20c4171f5a43594789675b2b814f590a83720

pr_000b:
  status: merged
  number: 3
  merge_performed: true
  merge_commit: 3211415c66e8461727a5ccfb7e6fddaee9bc20f5
  merged_at: "2026-06-21T12:42:43Z"

runtime:
  app: not_implemented
  github_actions: installed
  pages: not_configured
  branch_protection: active_ruleset
  auto_merge: disabled
  pipeline: not_installed
  production_release: not_applicable
```

The current PR head SHA must be read from GitHub PR metadata. A document cannot embed the SHA of the commit that contains itself without immediately making that value stale. The recorded SHA above is the verified head at Draft PR creation; the PR description records the current post-metadata head.

## Historical gate results

These are recorded as history only. They are bound to the head SHA shown and are **not** the
current gate results for any new head SHA. The latest Intent Review, Independent Verification,
External Audit, and Human Gate must be confirmed from GitHub PR comments, reviews, checks, or
other SHA-bound evidence for the current head SHA.

```yaml
historical_gate_results:
  independent_verification:
    id: PR-000A-IV-001
    head_sha: ed636a7f4a7405aa93714e9b0168be57c1622cf3
    result: blocked
  external_audit:
    id: PR-000A-EA-001
    head_sha: ed636a7f4a7405aa93714e9b0168be57c1622cf3
    result: fail
```

A new head SHA invalidates these results. Remediation that changes the head SHA requires new
Intent Review, Independent Verification, and External Audit bound to the new head SHA, each
under a new evidence ID.

## Context and governance

- Context audit and remediation: completed
- Final cross-document regression: completed with the documented Archive limitation retained in Google Drive
- Google Drive role before PR-000A merge: approved planning authority
- GitHub role: repository, branch, commit, pull request, diff, and check state authority
- PR-000A role: establish the first GitHub governance authority without runtime implementation

## Approved technical stack

```yaml
framework: React 19.2
language: TypeScript 6.0
build_tool: Vite 8
react_plugin: "@vitejs/plugin-react 6"
router: BrowserRouter
package_manager: npm
node_standard: "22.12 or later"
storage: browser localStorage
pwa: required
service_worker: required
backend: none
account: none
cloud_sync: none
```

The stack is approved but not installed in this PR.

## Repository decisions

```yaml
visibility: public
license: MIT
copyright_holder: Shunsuke Nagano
hosting: GitHub Pages
pages_project_path: /Pouro-Fable5-Re/
pages_enabled: false
custom_domain: not_required_for_initial_release
```

PR-000A corrects the LICENSE copyright line from `Shun` to `Shunsuke Nagano`. It does not change the MIT License text or enable Pages.

## Active blockers

- PR-000A, PR-000D, and PR-000B are merged to main (main HEAD: 3211415c66e8461727a5ccfb7e6fddaee9bc20f5). No governance PRs are currently open.
- GitHub Actions (docs-governance CI) is installed.
- Pages, pipeline runtime, and Production release remain unconfigured.
- Runtime, Recipe dataset, storage schema, PWA, and UI are not implemented.

## Next Human Gate

PR-000A, PR-000D, and PR-000B are merged. PR-000E (Post-merge Status Reconciliation) is in progress. The next Human decision is whether PR-000E may be merged after Intent Review, Independent Verification, External Audit, and docs-governance CI pass. Merge and Production deployment are separate; this gate does not authorize Production.

## Next planned PR

`PR-000E: Post-merge Status Reconciliation`, dependent on PR-000B merge. PR-000C (QA and Release Governance) follows after PR-000E.

## Authority transition

PR-000A is merged. This file is the Current Status authority on GitHub. Google Drive remains the authority for research, external evidence, pre-decision context, and long-term planning context unless a domain is intentionally migrated.
