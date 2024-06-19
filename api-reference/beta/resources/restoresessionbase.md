---
title: "restoreSessionBase resource type"
description: "Describes a restore session and its properties"
author: "tushar20"
ms.reviewer: "manikantsinghms"
ms.localizationpriority: medium
ms.subservice: "m365-backup-storage"
doc_type: resourcePageType
---

# restoreSessionBase resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a restore session for a [protection unit](protectionunitbase.md) that's protected by a [protection policy](protectionpolicybase.md). APIs are used by Global Admin or SharePoint Online Admin for SharePoint Online/OneDrive & Exchange Online Admin for Exchange Online to perform restore related tasks on artifacts which are protected as part of Protection Policy.

## Methods

|Method|Return type|Description|
|:---|:---|:---|
|[List](../api/backuprestoreroot-list-restoresessions.md)|[restoreSessionBase](../resources/restoresessionbase.md) collection|Get a list of  [restoreSessionBase](../resources/restoresessionbase.md) objects and their properties.|
|[Get](../api/restoresessionbase-get.md)|[restoreSessionBase](../resources/restoresessionbase.md)|Read the properties and relationships of a [restoreSessionBase](../resources/restoresessionbase.md) object.|
|[Delete](../api/restoresessionbase-delete.md)|None|Delete a [restoreSessionBase](../resources/restoresessionbase.md) object.|
|[Activate](../api/restoresessionbase-activate.md)|[restoreSessionBase](../resources/restoresessionbase.md)|Activate a draft restore session.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|id|String|The unique identifier of the restore session.|
|completedDateTime|DateTimeOffset|The time of completion of the restore session.|
|createdBy|identitySet|The identity of person who created the restore session.|
|createdDateTime|DateTimeOffset|The time of creation of the restore session.|
|error|publicError|Contains error details if the restore session fails or completes with an error.|
|lastModifiedBy|identitySet|Identity of the person who last modified the restore session.|
|lastModifiedDateTime|DateTimeOffset|Timestamp of the last modification of the restore session.|
|status|[restoreSessionStatus](../resources/restoresessionbase.md#restoresessionstatus-values)|Status of the restore session. The value is an aggregated status of the restored artifacts. The possible values are: `draft`, `activating`, `active`, `completedWithError`, `completed`, `unknownFutureValue`, `failed`. Note that you must use the `Prefer: include-unknown-enum-members` request header to get the following value in this [evolvable enum](/graph/best-practices-concept#handling-future-members-in-evolvable-enumerations): `failed`.|

### restoreSessionStatus values

|Member | Description |
|:------|:------------|
|draft|All artifacts are added.|
|activating|All artifacts are scheduled.|
|active|All or any restore artifacts are scheduled or in progress.|
|completedWithError|Some artifacts failed to restore, and some succeeded.|
|completed| All restore artifacts successfully restored.|
|failed| All restore artifacts failed to restore.|
|unknownFutureValue| Evolvable enumeration sentinel value. Do not use.|

## Relationships

None.

## JSON representation

The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.restoreSessionBase",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.restoreSessionBase",
  "id": "String (identifier)",
  "status": "String",
  "createdDateTime": "String (timestamp)",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "completedDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "lastModifiedBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "error": {
    "@odata.type": "microsoft.graph.publicError"
  }
}
```
