---
title: "mobileAppRelationship resource type"
description: "Describes a relationship between two mobile apps."
author: "jaiprakashmb"
localization_priority: Normal
ms.subservice: "intune"
doc_type: resourcePageType
---

# mobileAppRelationship resource type

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Describes a relationship between two mobile apps.

## Methods
|Method|Return Type|Description|
|:---|:---|:---|
|[List mobileAppRelationships](../api/intune-apps-mobileapprelationship-list.md)|[mobileAppRelationship](../resources/intune-apps-mobileapprelationship.md) collection|List properties and relationships of the [mobileAppRelationship](../resources/intune-apps-mobileapprelationship.md) objects.|
|[Get mobileAppRelationship](../api/intune-apps-mobileapprelationship-get.md)|[mobileAppRelationship](../resources/intune-apps-mobileapprelationship.md)|Read properties and relationships of the [mobileAppRelationship](../resources/intune-apps-mobileapprelationship.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|The relationship entity id.|
|targetId|String|The target mobile app's app id.|
|targetDisplayName|String|The target mobile app's display name. This property is read-only.|
|targetDisplayVersion|String|The target mobile app's display version. This property is read-only.|
|targetPublisher|String|The target mobile app's publisher. This property is read-only.|
|targetType|[mobileAppRelationshipType](../resources/intune-apps-mobileapprelationshiptype.md)|The type of relationship indicating whether the target is a parent or child. This property is read-only. Possible values are: `child`, `parent`.|

## Relationships
None

## JSON Representation
Here is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppRelationship"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppRelationship",
  "id": "String (identifier)",
  "targetId": "String",
  "targetDisplayName": "String",
  "targetDisplayVersion": "String",
  "targetPublisher": "String",
  "targetType": "String"
}
```