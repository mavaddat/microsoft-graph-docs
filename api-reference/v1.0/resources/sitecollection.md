---
author: spgraph-docs-team
ms.date: 09/10/2017
title: siteCollection resource type
ms.localizationpriority: medium
ms.subservice: "sharepoint"
description: "Provides more information about a site collection."
doc_type: resourcePageType
---

# siteCollection resource type

Namespace: microsoft.graph

Provides more information about a site collection.

If a [**site**](site.md) resource has a non-null **siteCollection** property, then the site is a root site for a site collection.

## Properties

| Property name        | Type     | Description
|:---------------------|:---------|:---------------------------------------------------
| **dataLocationCode** | string   | The geographic region code for where this site collection resides. Only present for multi-geo tenants. Read-only.
| **hostname**         | string   | The hostname for the site collection. Read-only.
| **root**             | [root][] | If present, indicates that this is a root site collection in SharePoint. Read-only.
| **archivalDetails**  | [siteArchivalDetails][] | Represents whether the site collection is recently archived, fully archived, or reactivating. Possible values are: `recentlyArchived`, `fullyArchived`, `reactivating`, `unknownFutureValue`.

## JSON representation

The following JSON representation shows the resource type.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
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
[siteArchivalDetails]: siteArchivalDetails.md

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Facets/SiteCollection"
}-->

