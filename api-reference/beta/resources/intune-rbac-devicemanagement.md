---
title: "deviceManagement resource type"
description: "Singleton entity that acts as a container for all device management functionality."
author: "jaiprakashmb"
localization_priority: Normal
ms.subservice: "intune"
doc_type: resourcePageType
---

# deviceManagement resource type

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Singleton entity that acts as a container for all device management functionality.

## Methods
|Method|Return Type|Description|
|:---|:---|:---|
|[Get deviceManagement](../api/intune-rbac-devicemanagement-get.md)|[deviceManagement](../resources/intune-shared-devicemanagement.md)|Read properties and relationships of the [deviceManagement](../resources/intune-shared-devicemanagement.md) object.|
|[Update deviceManagement](../api/intune-rbac-devicemanagement-update.md)|[deviceManagement](../resources/intune-shared-devicemanagement.md)|Update the properties of a [deviceManagement](../resources/intune-shared-devicemanagement.md) object.|
|[getEffectivePermissions function](../api/intune-rbac-devicemanagement-geteffectivepermissions.md)|String collection||
|[getEffectivePermissions function](../api/intune-rbac-devicemanagement-geteffectivepermissions.md)|[rolePermission](../resources/intune-rbac-rolepermission.md) collection||
|[getRoleScopeTagsByResource function](../api/intune-rbac-devicemanagement-getrolescopetagsbyresource.md)|[roleScopeTag](../resources/intune-rbac-rolescopetag.md) collection||
|[getRoleScopeTagsByIds function](../api/intune-rbac-devicemanagement-getrolescopetagsbyids.md)|[roleScopeTag](../resources/intune-rbac-rolescopetag.md) collection||
|[getAssignedRoleDetails function](../api/intune-rbac-devicemanagement-getassignedroledetails.md)|[deviceAndAppManagementAssignedRoleDetails](../resources/intune-rbac-deviceandappmanagementassignedroledetails.md)|Retrieves the assigned role definitions and role assignments of the currently authenticated user.|
|[scopedForResource function](../api/intune-rbac-devicemanagement-scopedforresource.md)|Boolean||

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String||

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|roleDefinitions|[roleDefinition](../resources/intune-rbac-roledefinition.md) collection|The Role Definitions.|
|roleAssignments|[deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) collection|The Role Assignments.|
|roleScopeTags|[roleScopeTag](../resources/intune-rbac-rolescopetag.md) collection|The Role Scope Tags.|
|resourceOperations|[resourceOperation](../resources/intune-rbac-resourceoperation.md) collection|The Resource Operations.|
|operationApprovalRequests|[operationApprovalRequest](../resources/intune-rbac-operationapprovalrequest.md) collection|The Operation Approval Requests|
|operationApprovalPolicies|[operationApprovalPolicy](../resources/intune-rbac-operationapprovalpolicy.md) collection|The Operation Approval Policies|

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