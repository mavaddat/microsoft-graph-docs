---
title: "deviceCategory resource type"
description: "Intune Devices Devicecategory Source_Resources ."
author: "jaiprakashmb"
localization_priority: Normal
ms.subservice: "intune"
doc_type: resourcePageType
---

# deviceCategory resource type

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.



## Methods
|Method|Return Type|Description|
|:---|:---|:---|
|[Get deviceCategory](../api/intune-devices-devicecategory-get.md)|[deviceCategory](../resources/intune-shared-devicecategory.md)|Read properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) object.|
|[Update deviceCategory](../api/intune-devices-devicecategory-update.md)|[deviceCategory](../resources/intune-shared-devicecategory.md)|Update the properties of a [deviceCategory](../resources/intune-shared-devicecategory.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|Unique identifier for the device category. Read-only.|

## Relationships
None

## JSON Representation
Here is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)"
}
```