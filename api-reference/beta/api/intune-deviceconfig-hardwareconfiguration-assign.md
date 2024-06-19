---
title: "assign action"
description: "Intune Deviceconfig Hardwareconfiguration Assign Api ."
author: "jaiprakashmb"
localization_priority: Normal
ms.subservice: "intune"
doc_type: apiPageType
---

# assign action

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.



[!INCLUDE [national-cloud-support](../../includes/all-clouds.md)]

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|DeviceManagementConfiguration.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|DeviceManagementConfiguration.ReadWrite.All|

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/hardwareConfigurations/{hardwareConfigurationId}/assign
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|
|Accept|application/json|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.

|Property|Type|Description|
|:---|:---|:---|
|hardwareConfigurationAssignments|[hardwareConfigurationAssignment](../resources/intune-deviceconfig-hardwareconfigurationassignment.md) collection||



## Response
If successful, this action returns a `200 OK` response code and a [hardwareConfigurationAssignment](../resources/intune-deviceconfig-hardwareconfigurationassignment.md) collection in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/hardwareConfigurations/{hardwareConfigurationId}/assign

Content-type: application/json
Content-length: 548

{
  "hardwareConfigurationAssignments": [
    {
      "@odata.type": "#microsoft.graph.hardwareConfigurationAssignment",
      "id": "2ab8e97c-e97c-2ab8-7ce9-b82a7ce9b82a",
      "target": {
        "@odata.type": "microsoft.graph.scopeTagGroupAssignmentTarget",
        "deviceAndAppManagementAssignmentFilterId": "Device And App Management Assignment Filter Id value",
        "deviceAndAppManagementAssignmentFilterType": "include",
        "targetType": "user",
        "entraObjectId": "Entra Object Id value"
      }
    }
  ]
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 521

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.hardwareConfigurationAssignment",
      "id": "2ab8e97c-e97c-2ab8-7ce9-b82a7ce9b82a",
      "target": {
        "@odata.type": "microsoft.graph.scopeTagGroupAssignmentTarget",
        "deviceAndAppManagementAssignmentFilterId": "Device And App Management Assignment Filter Id value",
        "deviceAndAppManagementAssignmentFilterType": "include",
        "targetType": "user",
        "entraObjectId": "Entra Object Id value"
      }
    }
  ]
}
```
