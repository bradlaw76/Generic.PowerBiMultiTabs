# Generic Power BI Multi-Tab Dashboard Development Guidelines

Auto-generated from project context. Last updated: 2026-02-19

## Active Technologies
- JavaScript (ES2020+) + React 18 (CDN) + Babel in-browser JSX + React 18 UMD, ReactDOM UMD, Tailwind CSS CDN, Dynamics 365 `Xrm.WebApi` (main)
- Dataverse (`genbbid_genericpbidashboard`) (main)

- JavaScript (ES2020+) + React 18 (CDN) + Tailwind CSS (CDN) + Babel (in-browser JSX)
- Dynamics 365 `Xrm.WebApi` + Dataverse entity `genbbid_genericpbidashboard`
- Power BI Embedded (autoAuth iframe)

## Project Structure

```text
genbbid_GenericPowerBIDashboardsSimple.html   # Simple single-iframe PBI embed
genbbid_pbi_dashboard.html                     # Multi-tab React dashboard
SYSTEM_MANIFEST.json.md                        # SpeckKit manifest (ux-demo)
UX_INVARIANTS.md                               # UX invariants
TEST_ACCEPTANCE.md                             # Acceptance checks
SPEC.md                                        # Optional project specification
CLAUDE.md                                      # Claude agent context
.github/copilot-instructions.md                # SpeckKit Copilot governance rules
.github/agents/copilot-instructions.md         # Specify Copilot agent context
.specify/                                      # Specify workflow files
```

## Commands

- No build step for web resources.
- Validate by loading web resources in a Dynamics 365 model-driven app.
- Optional local static check: open HTML files in browser and inspect console for script errors.

## Code Style

- Use functional React components with hooks only.
- Use Tailwind utility classes; avoid custom CSS unless required.
- Use `Xrm.WebApi.retrieveMultipleRecords` for Dataverse reads.
- Keep graceful error states; never leave blank UI.
- Preserve UX invariants in `UX_INVARIANTS.md`.

## Recent Changes
- main: Added JavaScript (ES2020+) + React 18 (CDN) + Babel in-browser JSX + React 18 UMD, ReactDOM UMD, Tailwind CSS CDN, Dynamics 365 `Xrm.WebApi`

- Added SpeckKit profile scaffolding (`SYSTEM_MANIFEST.json.md`, `UX_INVARIANTS.md`, `TEST_ACCEPTANCE.md`, `SPEC.md`).
- Added `.specify` templates, constitution, and PowerShell workflow scripts.

<!-- MANUAL ADDITIONS START -->
<!-- MANUAL ADDITIONS END -->
