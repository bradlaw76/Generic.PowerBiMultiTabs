# Data Model: Generic Power BI Multi-Tab Dashboard

## Entity: DashboardConfiguration
- **Source**: Dataverse entity `genbbid_genericpbidashboard`
- **Purpose**: Stores workspace branding and up to 5 embedded report tabs.

### Fields
- `id` (GUID, system)
- `statecode` (int)
  - `0` = Active
- `createdon` (datetime)
- `genbbid_workspacename` (string, optional, fallback: "Power BI Dashboard")
- `genbbid_brandcolorhex` (string, optional, fallback: `#0078D4`)
- `genbbid_tab1name` ... `genbbid_tab5name` (string, optional)
- `genbbid_tab1pbiembedcontent` ... `genbbid_tab5pbiembedcontent` (string, optional)

### Derived Model: DashboardTab
- `index` (1..5)
- `title` (string)
- `url` (string, normalized from raw URL or iframe snippet)

## Validation Rules
- Only records with `statecode = 0` are eligible.
- Record selection picks newest by `createdon desc`.
- Tab is included only when `tabNpbiembedcontent` yields a non-empty URL after normalization.
- Tab title falls back to `Tab N` when `tabNname` is missing.
- Brand color falls back to `#0078D4` when invalid or missing.

## Relationships
- One `DashboardConfiguration` produces zero-to-five `DashboardTab` entries at runtime.

## State Transitions
- `Draft/Inactive` (`statecode != 0`) → not rendered.
- `Active` (`statecode = 0`) → candidate for dashboard runtime.
- If multiple active records exist, latest `createdon` wins (effective active configuration).
