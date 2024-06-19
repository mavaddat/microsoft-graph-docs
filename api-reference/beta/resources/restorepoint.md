---
title: "restorePoint resource type"
description: "Represents the date and time when an artifact is protected by a protectionPolicy and can be restored."
author: "tushar20"
ms.reviewer: "manikantsinghms"
ms.localizationpriority: medium
ms.subservice: "m365-backup-storage"
doc_type: resourcePageType
---

# restorePoint resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the date and time when an [artifact](../resources/restoreartifactbase.md) is protected by a [protectionPolicy](../resources/protectionpolicybase.md) and can be restored.

## Methods

|Method|Return type|Description|
|:---|:---|:---|
|[List](../api/backuprestoreroot-list-restorepoints.md)|[restorePoint](../resources/restorepoint.md) collection|Get a list of [restorePoint](../resources/restorepoint.md) objects and their properties.|
|[Search](../api/restorepoint-search.md)|[restorePointSearchResponse](../resources/restorepointsearchresponse.md)|Search for the restore points associated with a [protectionUnit](../resources/protectionunitbase.md).|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|id|String|ID of the restore point.|
|protectionDateTime|DateTimeOffset|Date time when the restore point was created.|
|expirationDateTime|DateTimeOffset|Expiration date time of the restore point.|
|tags|[restorePointTags](../resources/restorepoint.md#restorepointtags-values)|The type of the restore point. The possible values are: `none`, `fastRestore`, `unknownFutureValue`.|

### restorePointTags values

|Member | Description |
|:------|:------------|
|none   | No tag.      |
|fastRestore | Get a fast restore point.|
|unknownFutureValue | Evolvable enumeration sentinel value. Do not use.|

## Relationships

|Relationship|Type|Description|
|:---|:---|:---|
|protectionUnit|[protectionUnitBase](../resources/protectionunitbase.md)|The site, drive, or mailbox units that are protected under a protection policy.|

## JSON representation

The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.restorePoint",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.restorePoint",
  "id": "String (identifier)",
  "protectionDateTime": "String (timestamp)",
  "expirationDateTime": "String (timestamp)",
  "tags": "String"
}
```
