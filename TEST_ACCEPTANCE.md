# Generic Power BI Multi-Tab Dashboard — Test Acceptance Criteria

**Status:** DRAFT
**Version:** 1.0.0
**Last Updated:** 2026-02-19

---

## Acceptance Tests

### Multi-Tab Dashboard (`genbbid_pbi_dashboard.html`)

#### Data Loading
- [ ] Dashboard loads without JavaScript errors when Xrm context is available
- [ ] Retrieves the most recent active record (`statecode eq 0`) from `genbbid_genericpbidashboard`
- [ ] Displays loading indicator while Dataverse query is in progress

#### Error Handling
- [ ] Shows "Xrm context not available" error when parent Xrm is missing
- [ ] Shows "No active dashboard configuration found" when no records match
- [ ] Retry button re-triggers the Dataverse query and clears previous error

#### Tab Rendering
- [ ] Renders tab bar when 2+ tabs have valid embed URLs
- [ ] Hides tab bar when only 1 tab is configured
- [ ] Active tab is highlighted with a bottom border accent
- [ ] Clicking a tab switches the iframe source without page reload
- [ ] Tab titles fall back to "Tab N" when `tabNname` field is empty

#### Iframe Embedding
- [ ] Power BI report renders inside a full-size, borderless iframe
- [ ] Extracts `src` from raw URL strings correctly
- [ ] Extracts `src` from `<iframe>` embed snippet strings correctly
- [ ] Shows "No dashboard tabs configured" when zero valid tabs exist

#### Branding
- [ ] Header background uses `brandcolorhex` from Dataverse record
- [ ] Falls back to `#0078D4` when no brand color is set
- [ ] Workspace name displays in the header from `workspacename` field

#### Footer
- [ ] Footer shows entity logical name (`genbbid_genericpbidashboard`)
- [ ] Footer shows current build version

---

### Simple Embed (`genbbid_GenericPowerBIDashboardsSimple.html`)

- [ ] Renders a single full-viewport iframe with no margin, padding, or border
- [ ] No header, footer, or tab chrome is visible
- [ ] Power BI report fills the entire browser window
