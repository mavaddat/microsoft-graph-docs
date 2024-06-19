---
title: "deviceManagement resource type"
description: "Singleton that acts as container for a collection of UserPFXCertificate entities."
author: "jaiprakashmb"
localization_priority: Normal
ms.subservice: "intune"
doc_type: resourcePageType
---

# deviceManagement resource type

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Singleton that acts as container for a collection of UserPFXCertificate entities.

## Methods
|Method|Return Type|Description|
|:---|:---|:---|
|[Get deviceManagement](../api/intune-raimportcerts-devicemanagement-get.md)|[deviceManagement](../resources/intune-shared-devicemanagement.md)|Read properties and relationships of the [deviceManagement](../resources/intune-shared-devicemanagement.md) object.|
|[Update deviceManagement](../api/intune-raimportcerts-devicemanagement-update.md)|[deviceManagement](../resources/intune-shared-devicemanagement.md)|Update the properties of a [deviceManagement](../resources/intune-shared-devicemanagement.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String||

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|userPfxCertificates|[userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) collection|Collection of PFX certificates associated with a user.|
|certificateConnectorDetails|[certificateConnectorDetails](../resources/intune-raimportcerts-certificateconnectordetails.md) collection|Collection of certificate connector details, each associated with a corresponding Intune Certificate Connector.|

## JSON Representation
Here is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)"
}
```