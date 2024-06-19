---
author: "spgraph-docs-team"
description: "Provides more information about a site collection."
title: "siteCollection resource type"
ms.localizationpriority: medium
ms.subservice: "sharepoint"
doc_type: resourcePageType
---

# siteCollection resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Provides more information about a site collection.

If a [**site**](site.md) resource has a non-null **siteCollection** property, the site is a root site for a site collection.

## Properties

| Property             | Type     | Description                                                                         |
| :------------------- | :------- | :---------------------------------------------------------------------------------- |
| **hostname**         | string   | The hostname for the site collection. Read-only.                                    |
| **dataLocationCode** | string   | The geographic region code for where this site collection resides. Only present for multi-geo tenants. Read-only.       |
| **root**             | [root][] | If present, indicates that this is a root site collection in SharePoint. Read-only. |
| **archivalDetails**  | [siteArchivalDetails][] | Represents whether the site collection is recently archived, fully archived, or reactivating. Possible values are: `recentlyArchived`, `fullyArchived`, `reactivating`, `unknownFutureValue`.  |


## JSON representation

The following JSON representation shows the resource type.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "dataLocationCode", "root"
  ],
  "@odata.type": "microsoft.graph.siteCollection"
}-->

```json
{
  "hostname": "contoso.sharepoint.com",
  "dataLocationCode": "EUR",
  "root": { "@odata.type": "microsoft.graph.root" },
  "archivalDetails": {
    "@odata.type": "microsoft.graph.siteArchivalDetails",
    "archiveStatus": "fullyArchived"
  }
}
```

[root]: root.md
[siteArchivalDetails]: sitearchivaldetails.md

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!--
{
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
