<!--
=============================================================================
DOCUMENT:     SpeckKit System Manifest — Generic Power BI Multi-Tab Dashboard
FILE:         SYSTEM_MANIFEST.json.md
VERSION:      1.0.0
AUTHOR:       bradlaw76
LAST UPDATED: 2026-02-19

-----------------------------------------------------------------------------
OVERVIEW
-----------------------------------------------------------------------------
System manifest for the Generic Power BI Multi-Tab Dashboard project.
Defines the project profile, registry linkage, code standards, and
review scope for SpeckKit governance.

-----------------------------------------------------------------------------
CHANGELOG
-----------------------------------------------------------------------------
v1.0.0  2026-02-19  Initial manifest — ux-demo profile
=============================================================================
-->

```jsonc
{
  "system": {
    "name": "Generic Power BI Multi-Tab Dashboard",
    "version": "1.4.7",
    "status": "DEVELOPMENT",
    "type": "ux-demo"
  },
  "purpose": {
    "summary": "A Dataverse-driven, multi-tab Power BI dashboard embed for Dynamics 365 / Power Pages. Reads configuration (tab names, embed URLs, brand color) from a Dataverse table and renders a tabbed React interface with dynamic iframe embedding."
  },
  "registry": {
    "indexUrl": "https://github.com/bradlaw76/SpeckKit-Project-Development/blob/main/system-manifests/MANIFEST_INDEX.json.md",
    "projectId": "generic-powerbi-multitab"
  },
  "review": {
    "speckitEnabled": true,
    "scope": ["ux", "acceptance"]
  },
  "codeStandards": {
    "source": "SpeckKit-Project-Development",
    "catalogUrl": "https://raw.githubusercontent.com/bradlaw76/SpeckKit-Project-Development/main/code-standards/CODE_STANDARDS_CATALOG.json.md",
    "standards": [
      {
        "id": "component-header-block",
        "url": "https://raw.githubusercontent.com/bradlaw76/SpeckKit-Project-Development/main/code-standards/comments/component-header-block.md",
        "defaultApply": true
      }
    ]
  },
  "uiReferences": {
    "source": "SpeckKit-Project-Development",
    "catalogUrl": "https://raw.githubusercontent.com/bradlaw76/SpeckKit-Project-Development/main/ui-references/UI_REFERENCE_CATALOG.json.md",
    "references": []
  },
  "projectReferences": {
    "description": "Other SpeckKit-governed projects this project depends on or relates to",
    "references": []
  }
}
```
