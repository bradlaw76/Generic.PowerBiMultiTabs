# Generic Power BI Multi-Tab Dashboard — Specification

**Status:** DRAFT
**Version:** 0.1.0
**Created:** 2026-02-19

---

## Purpose

A Dataverse-driven, configurable Power BI dashboard embed for Dynamics 365 and Power Pages. Allows administrators to define up to 5 tabbed Power BI reports via a single Dataverse record, with customizable tab names, embed URLs, workspace branding, and brand color theming.

## Scope

### In-Scope
- Multi-tab Power BI report embedding via Dataverse configuration
- Dynamic tab rendering (1–5 tabs) with iframe isolation
- Brand color theming from Dataverse field
- Simple single-report embed variant (no Dataverse dependency)
- Error handling and retry for Xrm / Dataverse failures

### Out-of-Scope
- Power BI authentication / token management (delegated to `autoAuth`)
- Dataverse record CRUD (admin creates records directly)
- Mobile-optimized responsive layouts (current: desktop-first)

## Requirements

### Functional
1. Read active dashboard configuration from `genbbid_genericpbidashboard` entity
2. Render 1–5 Power BI report tabs based on configured embed URLs
3. Support both raw URLs and `<iframe>` embed snippet inputs
4. Apply brand color from Dataverse to header bar
5. Show meaningful error states with retry capability

### Non-Functional
1. Must load within Dynamics 365 model-driven app iframe context
2. Must not introduce additional authentication prompts
3. Must render at 100% viewport with no layout jank
