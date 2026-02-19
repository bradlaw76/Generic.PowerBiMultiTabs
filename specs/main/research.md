# Research: Generic Power BI Multi-Tab Dashboard

## Decision 1: Runtime architecture remains client-side HTML + React + Dataverse read
- **Decision**: Keep browser-hosted React (CDN/Babel) with `Xrm.WebApi.retrieveMultipleRecords` directly from Dynamics context.
- **Rationale**: Matches existing production behavior, avoids introducing backend services, and aligns with constitution principle V (Simplicity & Incrementalism).
- **Alternatives considered**:
  - Backend proxy API for config: rejected due to unnecessary complexity and new auth boundary.
  - Build pipeline migration (bundled SPA): deferred; not required for this planning scope.

## Decision 2: Configuration source is a single active Dataverse record
- **Decision**: Use entity `genbbid_genericpbidashboard` with active filter (`statecode eq 0`) and latest record precedence (`createdon desc`).
- **Rationale**: Consistent with current implementation and constitution principle I (Configuration-Driven).
- **Alternatives considered**:
  - Multiple active records merged: rejected; increases ambiguity and conflicts.
  - Hardcoded defaults per environment: rejected; violates configuration-driven requirement.

## Decision 3: Embed URL normalization strategy
- **Decision**: Preserve `extractSrc()` behavior to accept both raw URLs and pasted `<iframe>` snippets.
- **Rationale**: Supports real admin input patterns and reduces config input errors.
- **Alternatives considered**:
  - Raw URLs only: rejected due to lower admin usability.
  - Full iframe HTML storage/rendering: rejected for security and sanitization complexity.

## Decision 4: Error and loading states are mandatory UX behaviors
- **Decision**: Keep explicit loading indicator, user-facing error panel, and Retry action for Xrm/Dataverse failures.
- **Rationale**: Required by constitution principle III (Graceful Degradation) and UX invariants.
- **Alternatives considered**:
  - Silent fallback / blank state: rejected as non-compliant.

## Decision 5: Performance and constraints for planning
- **Decision**:
  - UI shell should render within 1 second after HTML load in normal enterprise desktop conditions.
  - Dataverse config retrieval target: complete within 2 seconds p95 in tenant-normal conditions.
  - Max 5 tabs, desktop-first layout, no additional auth prompts.
- **Rationale**: Concrete and testable planning targets aligned with current design and non-functional requirements.
- **Alternatives considered**:
  - Tight sub-500ms end-to-end target: unrealistic due to external Power BI network dependency.

## Decision 6: Contract style for this feature
- **Decision**: Define a lightweight REST contract for "active dashboard config retrieval" as a design artifact.
- **Rationale**: Satisfies planning requirement for contracts while preserving current direct Dataverse implementation.
- **Alternatives considered**:
  - No contract artifact: rejected due to plan workflow requirement.
  - GraphQL schema: not needed for current single-resource read flow.
