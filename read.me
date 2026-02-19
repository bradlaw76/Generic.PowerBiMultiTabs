# Generic Power BI Multi-Tab Dashboard

<div align="center">

![Version](https://img.shields.io/badge/version-1.4.7-blue)
![Status](https://img.shields.io/badge/status-development-orange)
![Profile](https://img.shields.io/badge/SpeckKit-ux--demo-purple)
![React](https://img.shields.io/badge/React-18-61dafb?logo=react)
![Tailwind](https://img.shields.io/badge/Tailwind-CSS-38bdf8?logo=tailwindcss)
![Dynamics 365](https://img.shields.io/badge/Dynamics_365-Power_Platform-742774?logo=microsoft)

</div>

> 🚀 A Dataverse-driven, configurable Power BI dashboard embed for Dynamics 365 and Power Pages. Features dynamic multi-tab navigation, brand theming, and robust error handling.

---

## 📋 Table of Contents

- [Features](#-features)
- [Architecture](#-architecture)
  - [System Overview](#system-overview)
  - [Data Flow](#data-flow)
  - [Technology Stack](#technology-stack)
  - [Data Model](#data-model)
- [SpeckKit Integration](#-speckkit-integration)
- [Specify Workflow](#️-specify-workflow-spec-driven-development)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Development Workflow](#-development-workflow)
- [Testing](#-testing)
- [Documentation](#-documentation)
- [Performance & Security](#-performance--security)
- [Contributing](#-contributing)

---

## ✨ Features

### Multi-Tab Dashboard (`genbbid_pbi_dashboard.html`)
- **Dynamic Configuration**: Reads dashboard settings from Dataverse entity `genbbid_genericpbidashboard`
- **Up to 5 Tabs**: Configure 1-5 Power BI report tabs with custom names and embed URLs
- **Brand Theming**: Customizable header color from Dataverse configuration
- **Graceful Degradation**: User-friendly error states with retry capability
- **URL Flexibility**: Accepts both raw Power BI URLs and pasted iframe snippets
- **Loading States**: Clear visual feedback during data retrieval

### Simple Embed (`genbbid_GenericPowerBIDashboardsSimple.html`)
- **Zero Chrome**: Full-viewport single iframe with no header, tabs, or footer
- **Static Configuration**: Hardcoded embed URL for maximum simplicity
- **Instant Load**: No Dataverse dependency

---

## Architecture

### Technology Stack
- **JavaScript**: ES2020+ with arrow functions, template literals, async/await
- **React**: 18 (CDN) with in-browser Babel JSX transpilation
- **Styling**: Tailwind CSS (CDN)
- **Data Access**: Dynamics 365 `Xrm.WebApi.retrieveMultipleRecords`
- **Storage**: Dataverse entity `genbbid_genericpbidashboard`
- **Authentication**: Xrm session context + Power BI autoAuth

### Data Model
- **Entity**: `genbbid_genericpbidashboard`
- **Active Filter**: `statecode eq 0`
- **Record Selection**: Most recent by `createdon desc`
- **Configuration Fields**:
  - `genbbid_workspacename` (text)
  - `genbbid_brandcolorhex` (text, e.g., `#0078D4`)
  - `genbbid_tab1name` through `genbbid_tab5name` (text)
  - `genbbid_tab1pbiembedcontent` through `genbbid_tab5pbiembedcontent` (text)

---

## SpeckKit Integration

This project is governed by [SpeckKit](https://github.com/bradlaw76/SpeckKit-Project-Development) — a centralized registry for code standards, UI references, and project governance.

### Registry Information
- **Project ID**: `generic-powerbi-multitab`
- **Manifest Index**: v1.3
- **Profile**: `ux-demo`

### Governance Files
- `SYSTEM_MANIFEST.json.md` — Project manifest and registry linkage
- `UX_INVARIANTS.md` — Non-negotiable UX behaviors
- `TEST_ACCEPTANCE.md` — Acceptance test criteria
- `.github/copilot-instructions.md` — SpeckKit agent behavior rules

### Code Standards
- **Component Headers**: Auto-applied to all component files
- **Conventional Commits**: Required for all changes (`feat:`, `fix:`, `chore:`, `docs:`)
- **Constitution Compliance**: All changes validated against project constitution

---

## Specify Workflow (Spec-Driven Development)

The project uses the Specify workflow for structured feature development.

### Workflow Commands
```bash
# Initialize planning for current feature
specify init . --ai copilot

# Generate implementation plan
# (Executes via Copilot prompt: .github/prompts/speckit.plan.prompt.md)

# Generate actionable tasks
# (Executes via Copilot prompt: .github/prompts/speckit.tasks.prompt.md)

# Implement features
# (Executes via Copilot prompt: .github/prompts/speckit.implement.prompt.md)
```

### Planning Artifacts (`specs/main/`)
- `spec.md` — Feature specification with requirements
- `plan.md` — Technical context, constitution checks, structure decisions
- `research.md` — Architecture decisions and rationale
- `data-model.md` — Entity model and validation rules
- `contracts/` — OpenAPI/REST contract definitions
- `quickstart.md` — Validation scenarios

### Workflow Scripts (`.specify/scripts/powershell/`)
- `check-prerequisites.ps1` — Validate feature environment
- `create-new-feature.ps1` — Create new feature branch/folder
- `setup-plan.ps1` — Initialize plan.md from template
- `update-agent-context.ps1` — Refresh agent context files

---

## Project Structure

```
Generic.PowerBiMultiTabs/
├── genbbid_pbi_dashboard.html              # Multi-tab dashboard (v1.4.7)
├── genbbid_GenericPowerBIDashboardsSimple.html  # Simple single iframe
├── SYSTEM_MANIFEST.json.md                 # SpeckKit manifest
├── UX_INVARIANTS.md                        # UX invariant definitions
├── TEST_ACCEPTANCE.md                      # Acceptance criteria
├── SPEC.md                                 # Project specification
├── CLAUDE.md                               # Claude agent context
├── .github/
│   ├── copilot-instructions.md             # SpeckKit Copilot rules
│   ├── agents/                             # SpeckKit agent definitions
│   │   ├── copilot-instructions.md         # Copilot context (auto-updated)
│   │   ├── speckit.plan.agent.md
│   │   ├── speckit.tasks.agent.md
│   │   ├── speckit.implement.agent.md
│   │   └── ...
│   └── prompts/                            # Copilot prompt registrations
│       ├── speckit.plan.prompt.md
│       ├── speckit.tasks.prompt.md
│       └── ...
├── .specify/
│   ├── memory/
│   │   └── constitution.md                 # Project constitution
│   ├── templates/                          # Spec/plan/task templates
│   └── scripts/powershell/                 # Workflow automation
├── .vscode/
│   └── settings.json                       # VS Code Copilot integration
└── specs/
    └── main/                               # Current feature planning
        ├── spec.md
        ├── plan.md
        ├── research.md
        ├── data-model.md
        ├── quickstart.md
        └── contracts/
            └── dashboard-config.openapi.yaml
```

---

## Getting Started

### Prerequisites
1. Dynamics 365 environment with model-driven app
2. Dataverse table `genbbid_genericpbidashboard` deployed
3. At least one active dashboard configuration record
4. User read access to the entity
5. Valid Power BI report embed URLs with autoAuth enabled

### Deployment
1. Upload `genbbid_pbi_dashboard.html` as a web resource in Dynamics 365
2. Create a dashboard configuration record in `genbbid_genericpbidashboard`:
   - Set `statecode = 0` (Active)
   - Configure `workspacename` and `brandcolorhex`
   - Add 1-5 tab names and Power BI embed URLs
3. Embed the web resource in your model-driven app

### Configuration Example
```javascript
// Dataverse record fields
{
  "genbbid_workspacename": "Sales Dashboard",
  "genbbid_brandcolorhex": "#0078D4",
  "genbbid_tab1name": "Overview",
  "genbbid_tab1pbiembedcontent": "https://app.powerbi.com/reportEmbed?reportId=...",
  "genbbid_tab2name": "Details",
  "genbbid_tab2pbiembedcontent": "<iframe src='https://app.powerbi.com/...'></iframe>"
}
```

---

## Development Workflow

### Constitution Principles
1. **Configuration-Driven**: All behavior from Dataverse (no hardcoded URLs in multi-tab variant)
2. **Profile-Driven Compliance**: Adherence to SpeckKit `ux-demo` profile requirements
3. **Graceful Degradation**: User-friendly errors, never blank screens
4. **UX Invariant Preservation**: Changes must not violate documented invariants
5. **Simplicity & Incrementalism**: Ship working increments, avoid premature abstraction

### Making Changes
1. Review `UX_INVARIANTS.md` before any UI changes
2. Apply SpeckKit component header comments (auto-applied by Copilot)
3. Update `TEST_ACCEPTANCE.md` checklist after behavioral changes
4. Use conventional commits: `feat:`, `fix:`, `chore:`, `docs:`
5. Validate constitution compliance before merge

### Agent Support
- **Claude**: Use `CLAUDE.md` for Claude Code/CLI context
- **Copilot**: Use `.github/agents/copilot-instructions.md` (auto-updated from plan.md)

---

## Testing

### Manual Acceptance Tests
Run through checklist in `TEST_ACCEPTANCE.md`:
- Data loading and error handling
- Tab rendering and switching
- Iframe embedding (raw URLs and iframe snippets)
- Brand theming and workspace name display
- Loading states and retry functionality

### Quickstart Scenarios
Validate scenarios in `specs/main/quickstart.md`:
- Happy path (multi-tab)
- Single tab (tab bar hidden)
- Error handling (Xrm/Dataverse failures)
- Simple variant (zero chrome)

---

## Documentation

### Project Documentation
- `SPEC.md` — High-level project specification
- `CLAUDE.md` — Agent context with tech stack and conventions
- `UX_INVARIANTS.md` — Non-negotiable UX behaviors
- `TEST_ACCEPTANCE.md` — Acceptance criteria

### Planning Documentation (`specs/main/`)
- `spec.md` — Feature requirements
- `plan.md` — Implementation plan with constitution checks
- `research.md` — Architecture decisions
- `data-model.md` — Entity model
- `contracts/` — API contracts

### SpeckKit Registry
- Main registry: https://github.com/bradlaw76/SpeckKit-Project-Development
- Code standards catalog: [CODE_STANDARDS_CATALOG.json.md](https://raw.githubusercontent.com/bradlaw76/SpeckKit-Project-Development/main/code-standards/CODE_STANDARDS_CATALOG.json.md)
- UI references catalog: [UI_REFERENCE_CATALOG.json.md](https://raw.githubusercontent.com/bradlaw76/SpeckKit-Project-Development/main/ui-references/UI_REFERENCE_CATALOG.json.md)

---

## Performance

### Targets
- **UI Shell Render**: <1s after HTML load (desktop)
- **Dataverse Config Retrieval**: <2s p95 (normal tenant conditions)
- **Tab Switching**: Instant (no page reload)

### Constraints
- Maximum 5 tabs
- Desktop-first layout
- No additional authentication prompts
- Zero custom CSS (Tailwind utilities only)

---

## Security

- **Authentication**: Handled by Xrm.WebApi (Dynamics 365 session)
- **Power BI Auth**: Delegated to autoAuth (user's existing session)
- **No Token Management**: All auth handled by platform
- **Data Exposure**: Limited to dashboard config fields
- **Role Dependency**: Dynamics 365 security roles with entity read access

---

## Known Limitations

- Maximum 5 tabs (hardcoded loop)
- In-browser Babel transpilation (not production-build optimized)
- Tailwind CSS via CDN (intended for internal/demo usage)
- Desktop-first layout (mobile optimization out of scope)
- Client-side only (no SSR/pre-rendering)

---

## Contributing

1. Review project constitution in `.specify/memory/constitution.md`
2. Follow SpeckKit code standards (auto-applied)
3. Use Specify workflow for new features
4. Maintain UX invariants
5. Update acceptance tests
6. Use conventional commits

---

## License

[Specify license if applicable]

---

## Version History

- **v1.4.7** (2026-02-19): Added SpeckKit integration and complete planning artifacts
- **v1.4.7** (Prior): Initial multi-tab dashboard with React/Tailwind
- **v1.0.0**: Simple single-iframe embed variant

---

## Support

For issues or questions:
1. Review `TEST_ACCEPTANCE.md` for validation
2. Check `specs/main/quickstart.md` for scenarios
3. Consult `UX_INVARIANTS.md` for expected behavior
4. Review SpeckKit registry for governance questions
