# Project Charter

This charter is a high-level Project and Lifecycle Charter. It is **not** a detailed domain
specification. Detailed Feature Scope, Recipe Truth, Storage, Backup/Export/Import, UI, PWA,
and related specifications are governed by their dedicated Authorities recorded in
[docs/SOURCE_OF_TRUTH_INDEX.md](SOURCE_OF_TRUTH_INDEX.md). Where a domain is named below, this
charter records direction and defers exact values to that domain's Authority.

## 1. Project identity

- Project name: **Pourō-Fable5 Re**
- App and brand name: **Pourō**
- Repository: `NS-del346/Pouro-Fable5-Re`
- Product type: local-first hand-drip coffee guidance PWA
- Current lifecycle phase: Planning / Governance Foundation

## 2. Product purpose

Pourō-Fable5 Re is a quiet, local-first brew guide that reduces mental arithmetic, next-step
decisions, cumulative-water checks, Switch-operation mistakes, and friction when reusing
brewing conditions. Primary users are beginners through intermediate users practicing approved
brewing variants. Detailed feature scope is governed by the Feature Scope Authority.

## 3. High-level Out of Scope

The project does not include:

- accounts, mandatory backend services, or cloud sync
- social, community, marketplace, payments, subscriptions, or advertising
- automatic modification of Recipe Truth by an AI system
- measured or guaranteed TDS or extraction yield
- claims of being official, approved, supervised, endorsed, or a complete reproduction

Detailed inclusion and exclusion lists are governed by the Feature Scope Authority.

## 4. Repository identity

```yaml
repository: NS-del346/Pouro-Fable5-Re
visibility: public
default_branch: main
license: MIT
copyright_holder: Shunsuke Nagano
hosting: GitHub Pages
pages_project_path: /Pouro-Fable5-Re/
custom_domain: not_required_for_initial_release
```

GitHub Pages is an approved hosting direction but remains unconfigured. Enabling Pages and
performing a Production deployment require a separate Human Gate. The MIT License applies to
repository-owned software and documentation; it does not automatically license third-party
assets, fonts, trademarks, recipe sources, or quoted material. Detailed legal, attribution,
and NOTICE rules are governed by the Legal / Sources Authority.

## 5. Approved baseline direction (reference record)

The following directions were approved by Human decision on 2026-06-19 and are recorded here
as direction only. PR-000A does not install the runtime stack, dependencies, or any runtime.

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

Concrete dependency installation steps, exact configuration files, Storage namespaces and
schemas, PWA/Service Worker details, UI structure and terminology, and Backup/Export/Import
formats are deferred to their dedicated Authorities (see
[docs/SOURCE_OF_TRUTH_INDEX.md](SOURCE_OF_TRUTH_INDEX.md)). This charter does not duplicate
those specifications.

## 6. Recipe direction (reference record)

Initial implementation direction covers the 4:6 Method and approved variants, Classic Hybrid,
New Hybrid, 10 Pour / NEO, and Ice Brew / rapid-chill 4:6. Exact recipe values, ratios, steps,
temperatures, Switch states, New Hybrid Recipe Truth, source evidence, and implementation
eligibility are governed by the Recipe Truth Authority under its Human Gate. PR-000A does not
copy or implement recipe data.

## 7. Human Gate domains

Human approval is required for:

- Recipe Truth and scientific or source-evidence decisions
- legal, attribution, trademark, NOTICE, and public-copy decisions
- major information architecture or visual-direction decisions
- iPhone device, Safari, PWA standalone, Wake Lock, sound, and haptic acceptance
- storage migration, destructive data operations, and Import Replace
- dependency or license changes with material impact
- branch protection and ruleset final configuration
- Completion Contract changes
- repository visibility, Pages, Production deployment, and release

Approved specifications may be transcribed or mechanically validated within an explicit PR
contract, but unresolved Human Gate domains fail closed.

## 8. Lifecycle Authority

### Before PR-000A merge

- Google Drive is the approved planning authority.
- GitHub is the state authority for repository, branch, commit, pull request, diff, and checks.

### After PR-000A merge

- GitHub becomes the authority for code, runtime, PR state, QA evidence, release state, and
  Current Status.
- Google Drive remains the authority for research, external evidence, pre-decision context, and
  long-term planning context until a domain is intentionally migrated.
- The same complete specification must not be maintained independently in both locations.

Repository state always follows verified GitHub data.

## 9. Merge and Production deployment

PR merge, main integration, release-candidate creation, release approval, tag or GitHub Release
creation, Production deployment, and post-deploy smoke testing are separate lifecycle events.
Merging to `main` must not automatically publish Production. Production deployment requires an
approved release target and Human authorization.

## 10. Governance prerequisite and runtime status

Runtime is not implemented. PR-000A is docs-only and does not create a usable application.
Runtime implementation begins only through later PRs after governance, domain authorities,
required checks, and Human Gates are explicitly satisfied.

## 11. Human approval record

```yaml
approval_record:
  approval_id: HUMAN-2026-06-19-GOV-001
  approver: Shunsuke Nagano
  approval_date: 2026-06-19
  approval_channel: ChatGPT project conversation
  approved_directions:
    - technical configuration direction
    - public repository
    - MIT license
    - GitHub Pages hosting direction
    - initial Recipe dataset direction
    - Export and Import inclusion in initial release
    - New Hybrid Recipe Truth direction
  limitations:
    - does not authorize runtime implementation
    - does not authorize dependency installation
    - does not authorize Pages enablement
    - does not authorize Production deployment
    - does not authorize PR merge
    - does not replace domain-specific Recipe Truth
```

This approval is a **direction approval only**. It does not authorize the current head SHA, any
PR merge, runtime implementation, or Production deployment, and it does not replace
domain-specific Authorities such as Recipe Truth. Each merge and lifecycle gate must still be
satisfied independently for the current head SHA.
