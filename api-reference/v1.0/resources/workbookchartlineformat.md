---
title: "workbookChartLineFormat resource type"
description: "Encapsulates the formatting options for line elements."
author: "lumine2008"
ms.localizationpriority: medium
ms.subservice: "excel"
doc_type: resourcePageType
toc.title: Chart line format
---

# workbookChartLineFormat resource type

Namespace: microsoft.graph

Enapsulates the formatting options for line elements.


## Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get ChartLineFormat](../api/chartlineformat-get.md) | [workbookChartLineFormat](workbookchartlineformat.md) |Read properties and relationships of chartLineFormat object.|
|[Update](../api/chartlineformat-update.md) | [workbookChartLineFormat](workbookchartlineformat.md)	|Update ChartLineFormat object. |
|[Clear](../api/chartlineformat-clear.md)|None|Clear the line format of a chart element.|

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|color|string|HTML color code representing the color of lines in the chart.|

## Relationships
None


## JSON representation

The following JSON representation shows the resource type.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartLineFormat"
}-->

```json
{
  "color": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLineFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

