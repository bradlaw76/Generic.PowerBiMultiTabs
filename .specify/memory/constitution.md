# Generic Power BI Multi-Tab Dashboard Constitution

## Core Principles

### I. Configuration-Driven

All dashboard behavior — tab names, embed URLs, brand color, workspace name — MUST be driven by Dataverse configuration. No embed URLs, tab labels, or branding may be hardcoded in the multi-tab variant. The simple embed variant is the sole exception (single hardcoded URL by design).

### II. Profile-Driven Compliance

This project declares a SpeckKit `ux-demo` profile. Compliance is measured against the required files for that profile: `SYSTEM_MANIFEST.json.md`, `UX_INVARIANTS.md`, and `TEST_ACCEPTANCE.md`. The registry at `https://github.com/bradlaw76/SpeckKit-Project-Development` is the single source of truth for governance data.

### III. Graceful Degradation

The dashboard MUST never crash due to Xrm context unavailability, Dataverse query failures, or malformed embed URLs. Errors MUST be surfaced as user-friendly messages with a Retry action. The loading state MUST be shown while async work is in progress.

### IV. UX Invariant Preservation

UX invariants documented in `UX_INVARIANTS.md` are non-negotiable. No change may violate them without an explicit amendment to that file, a version increment, and documented rationale.

### V. Simplicity & Incrementalism

Start with the simplest solution that delivers value. The simple embed variant exists because not every deployment needs multi-tab Dataverse integration. Avoid premature abstraction. Ship working increments. Every commit MUST leave the project in a deployable state.

## Security & Authentication

- Xrm.WebApi handles authentication internally — no manual token management.
- Power BI autoAuth delegates identity to the user's existing session.
- No credentials, tokens, or secrets may be committed to source.
- Embed URLs may contain tenant IDs — treat them as semi-sensitive and avoid logging.

## Development Workflow

- All changes MUST be committed with descriptive conventional commit messages (`feat:`, `fix:`, `chore:`, `docs:`).
- Component files MUST carry the SpeckKit component header comment block (auto-applied).
- UX changes MUST be validated against `UX_INVARIANTS.md` before merge.
- The `TEST_ACCEPTANCE.md` checklist MUST be reviewed after any behavioral change.

## Governance

This constitution supersedes all ad-hoc practices. Amendments require:
1. A documented rationale for the change.
2. Version increment following semantic versioning (MAJOR for principle removal/redefinition, MINOR for additions, PATCH for clarifications).
3. Updated `LAST_AMENDED_DATE`.

All code reviews and audits MUST verify compliance with these principles.

**Version**: 1.0.0 | **Ratified**: 2026-02-19 | **Last Amended**: 2026-02-19
