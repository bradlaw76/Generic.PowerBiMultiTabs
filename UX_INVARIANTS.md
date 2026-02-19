# Generic Power BI Multi-Tab Dashboard — UX Invariants

**Status:** DRAFT
**Version:** 1.0.0
**Last Updated:** 2026-02-19

---

## Invariants

These UX behaviors must NEVER break across any version of the dashboard.

### Layout & Structure
- The dashboard must always render full-viewport (100% width, 100% height) with no scrollbar bleed.
- A branded header bar must always be visible at the top, showing the workspace name and a Refresh button.
- The footer must always be visible, showing the Dataverse entity name and the current build version.

### Tab Navigation
- When multiple tabs are configured, a horizontal tab bar must appear between the header and the content area.
- The active tab must be visually distinguished with a bottom border accent.
- Clicking a tab must immediately switch the embedded iframe — no full page reload.
- If only one tab is configured, the tab bar must be hidden entirely.

### Iframe Embedding
- Power BI reports must render inside a borderless, full-width, full-height iframe.
- The iframe `src` must be extracted correctly from both raw URLs and `<iframe>` embed snippets.
- If no tabs are configured, a "No dashboard tabs configured" placeholder must be shown.

### Loading & Error States
- A loading indicator must be shown while Dataverse data is being fetched.
- On Xrm context failure, a clear error message and Retry button must be displayed.
- On Dataverse query failure, a clear error message and Retry button must be displayed.

### Brand Theming
- The header background color must reflect the `brandcolorhex` field from Dataverse.
- If no brand color is configured, `#0078D4` (Fluent Blue) must be used as the default.

### Simple Embed Variant
- The simple embed variant (`genbbid_GenericPowerBIDashboardsSimple.html`) must render a single full-viewport iframe with zero chrome.
- No header, footer, or tabs — just the raw Power BI embed.
