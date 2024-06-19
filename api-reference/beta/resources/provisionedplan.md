---
title: "provisionedPlan resource type"
description: "The provisionedPlans property of the user entity and the organization entity is a collection of provisionedPlan objects."
ms.localizationpriority: medium
doc_type: resourcePageType
ms.subservice: "entra-directory-management"
author: "suawat"
---

# provisionedPlan resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Used by the **provisionedPlans** property of the [user](user.md) entity and the [organization](organization.md) entity.


## Properties
| Property       | Type    |Description|
|:---------------|:--------|:----------|
|capabilityStatus|String|For example, "Enabled".|
|provisioningStatus|String|For example, "Success".|
|service|String|The name of the service; for example, "AccessControlS2S"|

## JSON representation

The following JSON representation shows the resource type.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.provisionedPlan"
}-->

```json
{
  "capabilityStatus": "string",
  "provisioningStatus": "string",
  "service": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "provisionedPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


