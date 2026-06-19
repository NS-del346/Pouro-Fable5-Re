# Source of Truth Index

## 1. Purpose

This index identifies the authority for each project domain without duplicating complete specifications. Repository state is always determined from GitHub. Planning and domain material that has not yet been intentionally migrated remains in the active Google Drive authority.

Google Drive context root:

`https://drive.google.com/drive/folders/1ZP9AtvzdYyunxCnfXw-V4mnx4VQaIipT`

## 2. Global rules

- Current user instructions take priority within their authorized scope.
- Repository, branch, commit, pull request, diff, check, and merge state come from verified GitHub data.
- Before PR-000A merge, Google Drive is the approved planning authority.
- After PR-000A merge, GitHub is the authority for code, runtime, PR state, QA evidence, release state, and `docs/CURRENT_STATUS.md`.
- Domain specifications remain in their listed authority until deliberately migrated by a reviewed PR.
- Do not maintain the same complete specification independently in Google Drive and GitHub.
- Files marked Archive, Backup, Copy, Superseded, or `Do not execute` are not active authorities.
- A catalog entry does not prove that a feature or automation is implemented.
- Unresolved conflicts fail closed and are escalated to the applicable Human Gate.

## 3. Domain authority map

### Governance

```yaml
authority: GitHub governance documents after PR-000A merge; Google Drive approved planning authority before merge
location: docs/PROJECT_CHARTER.md, docs/CURRENT_STATUS.md, docs/SOURCE_OF_TRUTH_INDEX.md, and the active Google Drive governance documents
status: transition_in_progress
purpose: project identity, lifecycle authority, current status, conflict rules, and governance boundaries
```

### Product / Feature Scope

```yaml
authority: Pourō-Fable5 Re｜Feature Scope・Release Roadmap Source Context｜2026-06-19
location: Google Drive context root; migration target to be defined by PR-000B
status: active_drive_authority
purpose: approved features, initial-release inclusion, exclusions, and timing classification
```

### Recipe

```yaml
authority: Pourō-Fable5 Re｜Recipe Truth・Method Data Authority and approved evidence records
location: Google Drive context root until an explicit Recipe Truth migration PR
status: active_drive_authority_human_gate
purpose: recipe values, ratios, steps, temperatures, Switch states, source evidence, and implementation eligibility
```

### Legal / Attribution

```yaml
authority: Pourō-Fable5 Re｜Legal・Attribution・Source Policy
location: Google Drive context root until an explicit legal and NOTICE migration PR
status: active_drive_authority_human_gate
purpose: public wording, source use, trademarks, third-party rights, NOTICE, and attribution rules
```

### Storage / Migration

```yaml
authority: Pourō-Fable5 Re｜Storage・Data Model・Migration Authority
location: Google Drive context root until an explicit storage contract PR
status: active_drive_authority_human_gate
purpose: localStorage namespaces, schemas, migration, deletion boundaries, and compatibility
```

### Backup / Export / Import

```yaml
authority: Pourō-Fable5 Re｜Backup・Export・Import Format
location: Google Drive context root until an explicit data portability contract PR
status: active_drive_authority_human_gate
purpose: History CSV export, JSON backup and import, validation, preview, pre-import backup, Merge or Replace, verification, and rollback
```

### PWA / Deployment

```yaml
authority: Pourō-Fable5 Re｜PWA・Manifest・Service Worker・Deployment Authority and approved GitHub implementation after migration
location: Google Drive context root; future GitHub PWA specifications and runtime files
status: planned_not_implemented
purpose: manifest, Service Worker, cache namespace, GitHub Pages base path, offline behavior, and deployment boundaries
```

### UI / Terminology

```yaml
authority: Pourō-Fable5 Re｜UI画面構成・Viewport Priority and Pourō-Fable5 Re｜UI Terminology Matrix
location: Google Drive context root until an explicit UI authority migration PR
status: active_drive_authority
purpose: screen structure, viewport priority, Japanese and English terminology, and interaction language
```

### QA

```yaml
authority: Pourō-Fable5 Re｜QA・Acceptance・Evidence Policy; GitHub evidence bound to a head SHA after implementation
location: Google Drive context root and future GitHub PR checks, evidence, and QA records
status: policy_active_runtime_not_installed
purpose: required checks, N/A rules, device QA, evidence structure, invalidation, and acceptance criteria
```

### Release

```yaml
authority: Pourō-Fable5 Re｜Release・Deployment・Rollback Policy; GitHub release records after an approved release
location: Google Drive context root and future GitHub tags, releases, deployment records, and CURRENT_STATUS
status: policy_active_release_not_applicable
purpose: release candidate entry, Human approval, deployment, smoke testing, rollback, and incident handling
```

### PR Operations

```yaml
authority: docs/PR_BACKLOG.yaml, docs/COMPLETION_CONTRACT.yaml, .github/pull_request_template.md, PR contracts, and active Drive pipeline policies
location: GitHub repository and Google Drive context root
status: governance_foundation_in_progress_pipeline_not_installed
purpose: PR scope, dependencies, risk classification, allowed files, checks, Human Gates, verification, and merge controls
```

### AI Capability

```yaml
authority: dated AI Capability Status and model-routing documents
location: Google Drive context root and the actual execution environment
status: time_sensitive_verify_before_use
purpose: available model and tool capabilities, explicit model routing, and prohibition on assumed availability
```

### External Audit

```yaml
authority: Pourō-Fable5 Re｜External Audit Chat Operation Policy｜2026-06-19
location: Google Drive context root; audit results must identify repository, PR number, base SHA, head SHA, and context revisions
status: active_read_only_authority
purpose: independent Red Team review of governance, legal, data, PWA, release, major UI, and other high-risk domains
```

### Long Chat Handoff

```yaml
authority: Pourō-Fable5 Re｜Long Chat Handoff Operation Policy and the active Source of Truth Index
location: Google Drive context root and explicit handoff documents
status: active_operational_authority
purpose: preserve goals, sources, revisions, decisions, blockers, Human Gates, next actions, and prohibitions across chats
```

## 4. State versus intent

A Drive document may describe approved intent while GitHub still shows no implementation. In that case:

- Drive governs the approved product intent.
- GitHub governs whether files, workflows, Pages, releases, branches, PRs, and runtime actually exist.
- Documentation must not describe planned functionality as currently usable.

## 5. Archive exclusion

Search results may include copied, archived, backed-up, or superseded files. They must be excluded when any of the following is present:

- title contains `Archive`, `Backup`, `Copy`, `のコピー`, or `Superseded`
- title begins with `[ARCHIVED][SUPERSEDED]`
- body status says `Superseded / Do not execute`
- the active 00 Context Index identifies a newer authority

Archive material may be used only for historical comparison and must not independently authorize implementation or merge.
