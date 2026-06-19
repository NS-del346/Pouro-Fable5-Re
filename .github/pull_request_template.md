# Pull Request Contract

## Contract metadata

```yaml
pr_id: unresolved
type: unresolved
risk_classification: unresolved
human_gate: unresolved
intent_review_required: unresolved
external_audit_required: unresolved
auto_merge: false
base_sha: unresolved
head_sha: unresolved
```

Unresolved risk or gate values fail closed. `auto_merge: false` must not be changed without an approved PR contract and active repository safeguards.

## Goal

<!-- State the single independently verifiable outcome. -->

## Scope

<!-- List work included in this PR. -->

## Out of Scope

<!-- List adjacent work intentionally excluded. -->

## Source of Truth

<!-- Record exact authority titles, GitHub paths, Drive file IDs or URLs, revisions, and verification date. Do not use Archive, Backup, Copy, or Superseded documents as active authority. -->

## Allowed Files

```text
<!-- Exact allowlist -->
```

## Protected Files

```text
<!-- Files or patterns that must not change -->
```

## Risk Classification

```yaml
risk_classification: unresolved
risk_domains: []
reason: unresolved
```

## Human Gate

```yaml
human_gate: unresolved
stage: unresolved
reason: unresolved
approval_id: null
approved_head_sha: null
```

## Intent Review

```yaml
intent_review_required: unresolved
result: not_run
reviewer: null
evidence: null
```

## External Audit

```yaml
external_audit_required: unresolved
audit_id: null
result: not_run
audited_head_sha: null
blockers: []
```

## Changes

<!-- Summarize actual changes after implementation. -->

## Required Checks

- [ ] Base and head refs match the contract
- [ ] Changed files are within the allowlist
- [ ] Protected files are unchanged
- [ ] Diff/static validation passes
- [ ] Required structured files parse successfully
- [ ] Internal links resolve
- [ ] Security and secret review passes
- [ ] Domain-specific checks pass
- [ ] Any N/A check includes a reason

```yaml
checks:
  build: unresolved
  lint: unresolved
  typecheck: unresolved
  test: unresolved
  changed_files: unresolved
  protected_files: unresolved
  security: unresolved
  regression: unresolved
```

## Manual Verification

<!-- Record exact commands or inspection procedures, result, date, and verifier. -->

## Screenshots / Evidence

<!-- Provide screenshots, recordings, logs, or evidence links when applicable. State N/A with a reason when not applicable. -->

## Known Limitations

<!-- List unresolved limitations. Do not hide deferred work. -->

## Rollback

<!-- Explain how to revert this PR without rewriting main history or deleting user data. -->

## Self-report

```yaml
result: unresolved
head_sha: unresolved
changed_files: []
checks_passed: []
checks_n_a: []
known_limitations: []
merge_performed: false
```

## Independent Verification

```yaml
required: true
result: not_run
verified_head_sha: null
verifier: null
blockers: []
```

A head SHA, base SHA, changed-file set, acceptance criterion, required-check definition, Human decision, or Source of Truth revision change invalidates prior verification.

## Next PR

<!-- Identify only the next approved or tentative dependency. Do not overcommit future numbering or scope. -->

## 推奨されるモデル

Claude Codeで利用可能な最新のSonnetクラス。開始時に実際のモデル名とversionを確認する。利用可能性を推測しない。

## 最高の成果を期待する場合のモデル

利用可能な最新のOpusまたはFableクラス。AI Capability Statusおよび実行環境で利用可否を確認する。利用可能性を推測しない。

## Merge control

- [ ] All required checks are PASS or justified N/A
- [ ] Independent Verification is PASS for the current head SHA
- [ ] External Audit is complete when required
- [ ] Human Gate is explicitly satisfied when required
- [ ] No unresolved blocking review thread remains
- [ ] PR description and Current Status are consistent
- [ ] Production deployment is not implied by merge

```yaml
auto_merge: false
merge_authorized: false
production_deploy_authorized: false
```
