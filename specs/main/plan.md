# Implementation Plan: Generic Power BI Multi-Tab Dashboard

**Branch**: `main` | **Date**: 2026-02-19 | **Spec**: `/specs/main/spec.md`
**Input**: Feature specification from `/specs/main/spec.md`

**Note**: This template is filled in by the `/speckit.plan` command. See `.specify/templates/plan-template.md` for the execution workflow.

## Summary

Deliver a Dataverse-driven, configurable Power BI dashboard experience with up to five tabs, robust loading/error states, and strict UX invariant preservation. The technical approach keeps the existing browser-hosted React/Tailwind/Xrm.WebApi architecture and formalizes data model, contract, and operational guidance for consistent implementation.

## Technical Context

<!--
  ACTION REQUIRED: Replace the content in this section with the technical details
  for the project. The structure here is presented in advisory capacity to guide
  the iteration process.
-->

**Language/Version**: JavaScript (ES2020+) + React 18 (CDN) + Babel in-browser JSX  
**Primary Dependencies**: React 18 UMD, ReactDOM UMD, Tailwind CSS CDN, Dynamics 365 `Xrm.WebApi`  
**Storage**: Dataverse (`genbbid_genericpbidashboard`)  
**Testing**: Manual acceptance checklist in `TEST_ACCEPTANCE.md` + scenario validation in `quickstart.md`  
**Target Platform**: Dynamics 365 model-driven app iframe context (desktop-first)
**Project Type**: web  
**Performance Goals**: UI shell visible within 1s after HTML load; Dataverse config retrieval target <=2s p95 under normal tenant conditions  
**Constraints**: No added auth prompts; max 5 tabs; preserve existing UX invariants; no backend service addition in this scope  
**Scale/Scope**: Single dashboard record per runtime (latest active); up to 5 tabs per record

## Constitution Check

*GATE: Must pass before Phase 0 research. Re-check after Phase 1 design.*

### Pre-Design Gate Review
- **I. Configuration-Driven**: PASS — all multi-tab behavior sourced from Dataverse configuration.
- **II. Profile-Driven Compliance**: PASS — required `ux-demo` governance files present.
- **III. Graceful Degradation**: PASS — explicit loading and retry/error patterns retained.
- **IV. UX Invariant Preservation**: PASS — plan does not alter invariant behaviors.
- **V. Simplicity & Incrementalism**: PASS — no new backend abstractions introduced.

### Post-Design Gate Review
- **I. Configuration-Driven**: PASS — data model and contract reinforce active-record configuration retrieval.
- **II. Profile-Driven Compliance**: PASS — generated planning artifacts live under `specs/main` without governance drift.
- **III. Graceful Degradation**: PASS — quickstart and data model include failure/retry flows.
- **IV. UX Invariant Preservation**: PASS — tab, iframe, and loading/error expectations unchanged.
- **V. Simplicity & Incrementalism**: PASS — artifacts support incremental delivery with existing architecture.

## Project Structure

### Documentation (this feature)

```text
specs/main/
├── spec.md
├── plan.md
├── research.md
├── data-model.md
├── quickstart.md
├── contracts/
│   └── dashboard-config.openapi.yaml
└── tasks.md             # Phase 2 output (/speckit.tasks)
```

### Source Code (repository root)

```text
genbbid_pbi_dashboard.html
genbbid_GenericPowerBIDashboardsSimple.html
SYSTEM_MANIFEST.json.md
UX_INVARIANTS.md
TEST_ACCEPTANCE.md
SPEC.md
.github/
  copilot-instructions.md
  agents/
  prompts/
.specify/
  memory/
  scripts/powershell/
  templates/
specs/
  main/
```

**Structure Decision**: Existing single-web-resource HTML architecture retained; planning outputs are isolated in `specs/main`.

## Complexity Tracking

No constitution violations identified.
