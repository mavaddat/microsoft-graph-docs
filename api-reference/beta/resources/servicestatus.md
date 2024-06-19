---
title: "serviceStatus resource type"
description: "Represents the tenant-level service status of the backup service."
author: "tushar20"
ms.reviewer: "manikantsinghms"
ms.localizationpriority: medium
ms.subservice: "m365-backup-storage"
doc_type: resourcePageType
---

# serviceStatus resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the tenant-level service status of the backup service.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|backupServiceConsumer|[backupServiceConsumer](../resources/servicestatus.md#backupserviceconsumer-values)|The type of consumer. The possible values are: `unknown`, `firstparty`, `thirdparty`, `unknownFutureValue`.|
|disableReason|[disableReason](../resources/servicestatus.md#disablereason-values)|The reason the service is disabled. The possible values are: `none`, `invalidBillingProfile`, `userRequested`, `unknownFutureValue`.|
|gracePeriodDateTime|DateTimeOffset|The expiration time of the grace period.|
|lastModifiedBy|[identitySet](../resources/identityset.md)|Identity of the person who last modified the entity.|
|lastModifiedDateTime|DateTimeOffset|Timestamp of the last modification of the entity.|
|restoreAllowedTillDateTime|DateTimeOffset|The expiration time of the restoration allowed period.|
|status|[backupServiceStatus](../resources/servicestatus.md#backupservicestatus-values)|Status of the service. This value indicates what capabilities can be used. The possible values are: `disabled`, `enabled`, `protectionChangeLocked`, `restoreLocked`, `unknownFutureValue`.|

### backupServiceConsumer values

|Member | Description |
|:------|:------------|
|none | Default value. No consumer is using the service.|
|firstparty | Microsoft Admin Center is the backup service control app.|
|thirdparty | An ISV app is the backup service control app.|
|unknownFutureValue | Evolvable enumeration sentinel value. Do not use.|

### disableReason values

|Member | Description |
|:------|:------------|
|none | No reason specified.|
|invalidBillingProfile | Billing profile or Azure subscription status does not exist or is not healthy.|
|userRequested | Service is disabled manually via user action.|
|unknownFutureValue | Evolvable enumeration sentinel value. Do not use.|

### backupServiceStatus values

|Member | Description |
|:------|:------------|
|disabled | Service is disabled. This is the default state. The service is not enabled for the tenant.|
|enabled | Service is enabled. A new protection policy can be created or modified and restore is allowed.|
|protectionChangeLocked | Service is locked with no change in protection allowed. A new protection policy can't be created or updated. No new protection items can be added or removed.|
|restoreLocked | Service is locked with no protection change and no restore. The protection policy can't be created or updated. No new protection items can be added or removed. No restore can be performed.|
|unknownFutureValue | Evolvable enumeration sentinel value. Do not use.|

## Relationships

None.

## JSON representation

The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.serviceStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.serviceStatus",
  "status": "String",
  "gracePeriodDateTime": "String (timestamp)",
  "restoreAllowedTillDateTime": "String (timestamp)",
  "disableReason": "String",
  "backupServiceConsumer": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "lastModifiedBy": {
    "@odata.type": "microsoft.graph.identitySet"
  }
}
```
