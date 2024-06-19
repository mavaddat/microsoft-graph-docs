---
title: "authenticationConditionsApplications resource type"
description: "The applications on which an authenticationEventListener should trigger."
author: "soneff"
ms.localizationpriority: medium
ms.subservice: "entra-sign-in"
doc_type: resourcePageType
---

# authenticationConditionsApplications resource type

Namespace: microsoft.graph

The applications on which an authenticationEventListener should trigger.

## Properties
None.

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|includeApplications|[authenticationConditionApplication](../resources/authenticationconditionapplication.md) collection|Collection of the application conditions on which an authenticationEventListener should trigger.|

## JSON representation
The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.authenticationConditionsApplications"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.authenticationConditionsApplications"
}
```

