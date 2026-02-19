# Quickstart: Generic Power BI Multi-Tab Dashboard

## Goal
Validate the configured multi-tab dashboard behavior in a Dynamics 365 model-driven app.

## Prerequisites
- Dynamics 365 environment with access to `genbbid_genericpbidashboard`.
- At least one active dashboard configuration record (`statecode = 0`).
- Valid Power BI embed URLs (raw URL or iframe snippet accepted).

## Scenario A: Happy Path
1. Open the model-driven app page hosting `genbbid_pbi_dashboard.html`.
2. Confirm loading indicator appears during data fetch.
3. Confirm branded header appears with workspace name.
4. Confirm tabs render for each valid configured embed URL (up to 5).
5. Switch tabs and confirm iframe source updates without full-page reload.

## Scenario B: Single Tab
1. Configure exactly one valid tab URL.
2. Open dashboard and verify tab bar is hidden.
3. Confirm single iframe occupies content area.

## Scenario C: Error Handling
1. Temporarily remove/deny Xrm context or simulate Dataverse failure.
2. Verify user-facing error panel is shown.
3. Click Retry and confirm fetch is retried.

## Scenario D: Simple Variant
1. Open `genbbid_GenericPowerBIDashboardsSimple.html`.
2. Verify full-viewport borderless single iframe with no header, tabs, or footer.
