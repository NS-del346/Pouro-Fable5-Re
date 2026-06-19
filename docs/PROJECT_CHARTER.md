# Project Charter

## 1. Project identity

- Project name: **Pourō-Fable5 Re**
- App and brand name: **Pourō**
- Repository: `NS-del346/Pouro-Fable5-Re`
- Product type: local-first hand-drip coffee guidance PWA
- Current lifecycle phase: Planning / Governance Foundation

## 2. Product purpose

Pourō-Fable5 Re is a quiet brew guide intended to reduce mental arithmetic, next-step decisions, cumulative-water checks, Switch-operation mistakes, and friction when reusing brewing conditions.

Primary users are beginners through intermediate users practicing approved variants of the 4:6 Method, Hybrid brewing, 10 Pour / NEO, and Ice Brew, including users who want to scale an approved recipe to a supported coffee dose without using a complex analysis platform.

## 3. Core direction

- Local-first operation
- No account, backend, or cloud synchronization
- Installable PWA with an offline App Shell
- Portrait-first mobile interface
- Method selection as the primary entry point
- Explicit History saving; timer completion does not save automatically
- History as completed brew records
- My Recipes as reusable setup presets
- Quiet, premium, research-notebook, tool-like presentation

## 4. Out of Scope

The project does not include:

- accounts, mandatory backend services, or cloud sync
- social networking, community features, recipe marketplace, payments, subscriptions, or advertising
- automatic modification of Recipe Truth by an AI system
- measured or guaranteed TDS or extraction yield
- claims that the product is official, approved, supervised, endorsed, or a complete reproduction
- CSV import in the initial release

## 5. Approved technical stack

The following architecture was approved by Human decision on 2026-06-19:

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

This charter records the decision only. PR-000A does not install the runtime stack or dependencies.

## 6. Repository, licensing, and hosting

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

GitHub Pages is an approved hosting direction but remains unconfigured. Enabling Pages and performing a Production deployment require a separate Human Gate.

The MIT License applies to repository-owned software and documentation. It does not automatically license third-party assets, fonts, trademarks, recipe sources, or quoted material.

## 7. Initial release functional boundary

Approved initial-release product scope includes:

- Home and method selection
- Recipe Setup and Preview
- Active Brew / Timer
- Finish / Brew Log
- explicit Save to History
- History, History Detail, and Rebrew
- My Recipes as setup presets
- Settings, source information, and notices
- local-first storage
- PWA and offline foundation
- approved backup, export, and import capabilities

These are product requirements, not claims that the functions are currently implemented.

## 8. Initial Recipe scope

The initial implementation scope is approved for:

- 4:6 Method and approved variants
- Classic Hybrid
- New Hybrid
- 10 Pour / NEO
- Ice Brew / rapid-chill 4:6

Exact recipe values, steps, ratios, temperatures, Switch states, source evidence, and implementation eligibility remain governed by the Recipe Truth authority. PR-000A does not copy or implement recipe data.

## 9. Backup, Export, and Import

The initial release must include:

- History CSV export
- full JSON backup
- JSON import validation
- import preview
- automatic pre-import backup
- Merge and Replace modes
- destructive Replace confirmation
- read-back verification
- rollback handling
- offline/local execution without external data transmission

CSV import is Out of Scope.

## 10. Local data namespace

Approved namespace direction:

```text
pouroFable5Re.history.v1
pouroFable5Re.myRecipes.v1
pouroFable5Re.settings.v1
pouroFable5Re.activeBrew.v1
pouroFable5Re.lastSetup.v1
```

Old-project keys must not be reused directly. Migration or import must be explicit, and `localStorage.clear()` is prohibited.

## 11. Human Gate domains

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

Approved specifications may be transcribed or mechanically validated within an explicit PR contract, but unresolved Human Gate domains fail closed.

## 12. Lifecycle Authority

### Before PR-000A merge

- Google Drive is the approved planning authority.
- GitHub is the state authority for repository, branch, commit, pull request, diff, and checks.

### After PR-000A merge

- GitHub becomes the authority for code, runtime, PR state, QA evidence, release state, and Current Status.
- Google Drive remains the authority for research, external evidence, pre-decision context, and long-term planning context until a domain is intentionally migrated.
- The same complete specification must not be maintained independently in both locations.

Repository state always follows verified GitHub data.

## 13. Merge and Production deployment

PR merge, main integration, release-candidate creation, release approval, tag or GitHub Release creation, Production deployment, and post-deploy smoke testing are separate lifecycle events.

Merging to `main` must not automatically publish Production. Production deployment requires an approved release target and Human authorization.

## 14. Decision Pending

The following remain unresolved and must not be inferred:

- Minimal Brew Feedback schema
- sound and haptic initial scope
- final branch-protection and ruleset configuration
- detailed CI checks and workflow design
- Production release approval and timing
- future adoption of a custom domain

## 15. Governance prerequisite

Runtime implementation begins only through later PRs after governance, domain authorities, required checks, and Human Gates are explicitly satisfied. PR-000A is docs-only and does not create a usable application.
