---
title: "Assign administrative roles by using PIM for Microsoft Entra roles APIs"
description: "Learn how to create a role-assignable security group for IT Helpdesk and use the PIM API to assign the security group eligibility to the User Administrator role."
author: FaithOmbongi
ms.author: ombongifaith
ms.reviewer: rianakarim
ms.topic: tutorial
ms.localizationpriority: medium
ms.subservice: entra-id-governance
ms.date: 03/25/2024
#Customer intent: As a developer integrating with Microsoft Graph, I want to learn how to integrate PIM APIs for just in time access to Microsoft Entra roles, so that I can strengthen my organization's Zero Trust posture by enforcing the principle of least privilege.
---


# Assign administrative roles by using PIM for Microsoft Entra roles APIs

Privileged Identity Management (PIM) enables organizations to manage administrative access to resources in Microsoft Entra ID. The administrative access can be through role-assignable groups or Microsoft Entra roles. PIM helps to manage the risks of privileged access by limiting when access is active, managing the scope of access, and providing an auditable log of privileged access.

Contoso wants to assign administrative roles to principals using security groups. The company assigns eligibility instead of persistently active administrative roles. This method is effective in the following ways:
- Remove existing or adding more group members also removes administrators.
- Group members inherit the eligible role assignment. You can assign more roles to a group instead of assigning roles directly to individual users.
- Assigning eligibility instead of a persistently active User Administrator privilege allows the company to enforce **just-in-time access**, which grants temporary permissions to carry out the privileged tasks. When a group member needs to use the privileges, they activate their assignment for a temporary period. All records of role activations are auditable by the company.

In this tutorial, you learn how to:

> [!div class="checklist"]
> * Create a role-assignable security group.
> * Make a role-assignable security group eligible to an administrative role.
> * Grant just-in-time access to a user by activating their eligible assignment. 

## Prerequisites

To complete this tutorial, you need the following resources and privileges:

+ A working Microsoft Entra tenant with a Microsoft Entra ID P2 or Microsoft Entra ID Governance license enabled. 
+ Sign in to an API client such as [Graph Explorer](https://aka.ms/ge) to call Microsoft Graph with an account that has at least the *Privileged Role Administrator* role.
  + [Optional] Start a new anonymous session in another browser. You sign in later in this tutorial.
A test user that's enabled for MFA and you have access to their Microsoft Authenticator app account.
+ Grant yourself the following delegated permissions: `Group.ReadWrite.All`, `Directory.Read.All`, `RoleEligibilitySchedule.ReadWrite.Directory`, and `RoleAssignmentSchedule.ReadWrite.Directory`, and `RoleManagement.ReadWrite.Directory`.

## Step 1: Create a role-assignable security group

Assign yourself as the group owner and both you and the test user as members.

### Request: Create a role-assignable group

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "tutorial-assignaadroles-createSecurityGroup"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups
Content-type: application/json

{
    "description": "IT Helpdesk to support Contoso employees",
    "displayName": "IT Helpdesk (User)",
    "mailEnabled": false,
    "mailNickname": "userHelpdesk",
    "securityEnabled": true,
    "isAssignableToRole": true,
    "owners@odata.bind": [
        "https://graph.microsoft.com/v1.0/users/1ed8ac56-4827-4733-8f80-86adc2e67db5"
    ],
    "members@odata.bind": [
        "https://graph.microsoft.com/v1.0/users/1ed8ac56-4827-4733-8f80-86adc2e67db5",
        "https://graph.microsoft.com/v1.0/users/7146daa8-1b4b-4a66-b2f7-cf593d03c8d2"
    ]
}
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/v1/tutorial-assignaadroles-createsecuritygroup-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/v1/tutorial-assignaadroles-createsecuritygroup-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/v1/tutorial-assignaadroles-createsecuritygroup-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/v1/tutorial-assignaadroles-createsecuritygroup-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/v1/tutorial-assignaadroles-createsecuritygroup-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/v1/tutorial-assignaadroles-createsecuritygroup-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/v1/tutorial-assignaadroles-createsecuritygroup-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/v1/tutorial-assignaadroles-createsecuritygroup-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

> **Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups/$entity",
    "@odata.id": "https://graph.microsoft.com/v2/29a4f813-9274-4e1b-858d-0afa98ae66d4/directoryObjects/e77cbb23-0ff2-4e18-819c-690f58269752/Microsoft.DirectoryServices.Group",
    "id": "e77cbb23-0ff2-4e18-819c-690f58269752",
    "description": "IT Helpdesk to support Contoso employees",
    "displayName": "IT Helpdesk (User)",
    "groupTypes": [],
    "isAssignableToRole": true,
    "mailEnabled": false,
    "mailNickname": "userHelpdesk",
    "securityEnabled": true,
    "securityIdentifier": "S-1-12-1-3883711267-1310199794-258579585-1385637464",
    "visibility": "Private",
    "onPremisesProvisioningErrors": []
}
```

## Step 2: Create a unifiedRoleEligibilityScheduleRequest

Now that you have a role-assignable security group, assign it as eligible for the User Administrator role for one year. Scope the eligible assignment to your entire tenant. This tenant-level scoping allows the user admin to use their privilege against all users in your tenant, except higher privileged users such as the Global Administrator.

### Request

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "tutorial-assignaadroles-unifiedRoleEligibilityScheduleRequest_create"
}-->
```http
POST https://graph.microsoft.com/v1.0/roleManagement/directory/roleEligibilityScheduleRequests
Content-type: application/json

{
    "action": "AdminAssign",
    "justification": "Assign User Admin eligibility to IT Helpdesk (User) group",
    "roleDefinitionId": "fe930be7-5e62-47db-91af-98c3a49a38b1",
    "directoryScopeId": "/",
    "principalId": "e77cbb23-0ff2-4e18-819c-690f58269752",
    "scheduleInfo": {
        "startDateTime": "2021-07-01T00:00:00Z",
        "expiration": {
            "endDateTime": "2022-06-30T00:00:00Z",
            "type": "AfterDateTime"
        }
    }
}
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/v1/tutorial-assignaadroles-unifiedroleeligibilityschedulerequest-create-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/v1/tutorial-assignaadroles-unifiedroleeligibilityschedulerequest-create-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/v1/tutorial-assignaadroles-unifiedroleeligibilityschedulerequest-create-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/v1/tutorial-assignaadroles-unifiedroleeligibilityschedulerequest-create-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/v1/tutorial-assignaadroles-unifiedroleeligibilityschedulerequest-create-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/v1/tutorial-assignaadroles-unifiedroleeligibilityschedulerequest-create-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/v1/tutorial-assignaadroles-unifiedroleeligibilityschedulerequest-create-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/v1/tutorial-assignaadroles-unifiedroleeligibilityschedulerequest-create-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

> **Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.unifiedRoleEligibilityScheduleRequests"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#roleManagement/directory/roleEligibilityScheduleRequests/$entity",
    "id": "64a8bd54-4591-4f6a-9c77-3e9cb1fdd29b",
    "status": "Provisioned",
    "createdDateTime": "2021-09-03T20:45:28.3848182Z",
    "completedDateTime": "2021-09-03T20:45:39.1194292Z",
    "action": "AdminAssign",
    "principalId": "e77cbb23-0ff2-4e18-819c-690f58269752",
    "roleDefinitionId": "fe930be7-5e62-47db-91af-98c3a49a38b1",
    "directoryScopeId": "/",
    "isValidationOnly": false,
    "targetScheduleId": "64a8bd54-4591-4f6a-9c77-3e9cb1fdd29b",
    "justification": "Assign User Admin eligibility to IT Helpdesk (User) group",
    "createdBy": {
        "user": {
            "id": "1ed8ac56-4827-4733-8f80-86adc2e67db5"
        }
    },
    "scheduleInfo": {
        "startDateTime": "2021-09-03T20:45:39.1194292Z",
        "expiration": {
            "type": "afterDateTime",
            "endDateTime": "2022-06-30T00:00:00Z"
        }
    },
    "ticketInfo": {}
}
```

## Step 3: Confirm the user's current role assignments

While the group members are now *eligible* for the User Administrator role, they're still unable to use the role unless they explicitly activate the role. You can confirm by checking the user's current role assignments.

### Request

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "tutorial-assignaadroles-roleAssignments_list"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/roleManagement/directory/roleAssignments?$filter=principalId eq '7146daa8-1b4b-4a66-b2f7-cf593d03c8d2'
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/v1/tutorial-assignaadroles-roleassignments-list-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/v1/tutorial-assignaadroles-roleassignments-list-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/v1/tutorial-assignaadroles-roleassignments-list-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/v1/tutorial-assignaadroles-roleassignments-list-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/v1/tutorial-assignaadroles-roleassignments-list-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/v1/tutorial-assignaadroles-roleassignments-list-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/v1/tutorial-assignaadroles-roleassignments-list-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/v1/tutorial-assignaadroles-roleassignments-list-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

> **Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.unifiedRoleAssignments"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#roleManagement/directory/roleAssignments",
    "value": []
}
```

The empty response object shows that the user has no existing Microsoft Entra roles in Contoso. The user will now activate their eligible User Administrator role for a limited time.

## Step 4: User self-activates their eligible assignment

An incident ticket CONTOSO: Security-012345 has been raised in Contoso's incident management system and the company requires that all employee's refresh tokens be invalidated. As a member of IT Helpdesk, Aline is responsible for fulfilling this task.

First, start the Authenticator app on your phone and open Aline Dupuy's account.

Sign in to Graph Explorer as Aline. You can use another browser for this step. By doing so, you won't interrupt your current session. Alternatively, you can interrupt your current session by signing out of Graph Explorer and signing back in as Aline.

After signing in, activate your User Administrator role for five hours.

### Request

To activate a role, call the `roleAssignmentScheduleRequests` endpoint. In this request, the `UserActivate` action allows you to activate your eligible assignment.

+ For **principalId**, supply the value of your (Aline's) **id**.
+ The **roleDefinitionId** is the **id** of the role you're eligible for, in this case, the User Administrator role.
+ Enter the details of the ticket system that provides an auditable justification for activating the request.


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "tutorial-assignaadroles-roleAssignmentScheduleRequests_selfActivate"
}-->
```http
POST https://graph.microsoft.com/v1.0/roleManagement/directory/roleAssignmentScheduleRequests
Content-type: application/json

{
    "action": "SelfActivate",
    "principalId": "7146daa8-1b4b-4a66-b2f7-cf593d03c8d2",
    "roleDefinitionId": "fe930be7-5e62-47db-91af-98c3a49a38b1",
    "directoryScopeId": "/",
    "justification": "Need to invalidate all app refresh tokens for Contoso users.",
    "scheduleInfo": {
        "startDateTime": "2024-03-25T15:13:00.000Z",
        "expiration": {
            "type": "AfterDuration",
            "duration": "PT5H"
        }
    },
    "ticketInfo": {
        "ticketNumber": "CONTOSO:Security-012345",
        "ticketSystem": "Contoso ICM"
    }
}
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/v1/tutorial-assignaadroles-roleassignmentschedulerequests-selfactivate-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/v1/tutorial-assignaadroles-roleassignmentschedulerequests-selfactivate-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/v1/tutorial-assignaadroles-roleassignmentschedulerequests-selfactivate-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/v1/tutorial-assignaadroles-roleassignmentschedulerequests-selfactivate-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/v1/tutorial-assignaadroles-roleassignmentschedulerequests-selfactivate-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/v1/tutorial-assignaadroles-roleassignmentschedulerequests-selfactivate-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/v1/tutorial-assignaadroles-roleassignmentschedulerequests-selfactivate-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/v1/tutorial-assignaadroles-roleassignmentschedulerequests-selfactivate-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

> **Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.roleEligibilityScheduleRequests"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#roleManagement/directory/roleAssignmentScheduleRequests/$entity",
    "id": "295edd40-4646-40ca-89b8-ab0b46b6f60e",
    "status": "Granted",
    "createdDateTime": "2021-09-03T21:10:49.6670479Z",
    "completedDateTime": "2021-09-04T15:13:00Z",
    "action": "SelfActivate",
    "principalId": "7146daa8-1b4b-4a66-b2f7-cf593d03c8d2",
    "roleDefinitionId": "fe930be7-5e62-47db-91af-98c3a49a38b1",
    "directoryScopeId": "/",
    "isValidationOnly": false,
    "targetScheduleId": "295edd40-4646-40ca-89b8-ab0b46b6f60e",
    "justification": "Need to invalidate all app refresh tokens for Contoso users.",
    "createdBy": {
        "user": {
            "id": "7146daa8-1b4b-4a66-b2f7-cf593d03c8d2"
        }
    },
    "scheduleInfo": {
        "startDateTime": "2021-09-04T15:13:00Z",
        "expiration": {
            "type": "afterDuration",
            "endDateTime": null,
            "duration": "PT5H"
        }
    },
    "ticketInfo": {
        "ticketNumber": "CONTOSO:Security-012345",
        "ticketSystem": "Contoso ICM"
    }
}
```

You can confirm your assignment by running `GET https://graph.microsoft.com/v1.0/roleManagement/directory/roleAssignmentScheduleRequests/filterByCurrentUser(on='principal')`. The response object returns your newly activated role assignment with its status set to `Granted`. With your new privilege, carry out any allowed actions within five hours your assignment is active for. After five hours, the active assignment expires but through your membership in the **IT Support (Users)** group, you're eligible for the User Administrator role.

## Step 6: Clean up resources

Sign in as the Privileged Role Administrator and delete the following resources that you created for this tutorial: the role eligibility request and IT Support (Users) group.

### Revoke the role eligibility request

#### Request

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "tutorial-assignaadroles-roleEligibilityScheduleRequests_revoke"
}-->
```http
POST https://graph.microsoft.com/v1.0/roleManagement/directory/roleEligibilityScheduleRequests
Content-type: application/json

{
    "action": "AdminRemove",
    "principalId": "e77cbb23-0ff2-4e18-819c-690f58269752",
    "roleDefinitionId": "fe930be7-5e62-47db-91af-98c3a49a38b1",
    "directoryScopeId": "/"
}

```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/v1/tutorial-assignaadroles-roleeligibilityschedulerequests-revoke-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/v1/tutorial-assignaadroles-roleeligibilityschedulerequests-revoke-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/v1/tutorial-assignaadroles-roleeligibilityschedulerequests-revoke-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/v1/tutorial-assignaadroles-roleeligibilityschedulerequests-revoke-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/v1/tutorial-assignaadroles-roleeligibilityschedulerequests-revoke-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/v1/tutorial-assignaadroles-roleeligibilityschedulerequests-revoke-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/v1/tutorial-assignaadroles-roleeligibilityschedulerequests-revoke-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/v1/tutorial-assignaadroles-roleeligibilityschedulerequests-revoke-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

#### Response

> **Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.roleEligibilityScheduleRequests"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#roleManagement/directory/roleEligibilityScheduleRequests/$entity",
    "id": "dcd11a1c-300f-4d17-8c7a-523830400ec8",
    "status": "Revoked",
    "action": "AdminRemove",
    "principalId": "e77cbb23-0ff2-4e18-819c-690f58269752",
    "roleDefinitionId": "fe930be7-5e62-47db-91af-98c3a49a38b1",
    "directoryScopeId": "/"
}
```

### Delete the IT Support (Users) group

The request returns a `204 No Content` response code.

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "tutorial-assignaadroles-group_delete"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/e77cbb23-0ff2-4e18-819c-690f58269752
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/v1/tutorial-assignaadroles-group-delete-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/v1/tutorial-assignaadroles-group-delete-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/v1/tutorial-assignaadroles-group-delete-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/v1/tutorial-assignaadroles-group-delete-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/v1/tutorial-assignaadroles-group-delete-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/v1/tutorial-assignaadroles-group-delete-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/v1/tutorial-assignaadroles-group-delete-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/v1/tutorial-assignaadroles-group-delete-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

## Conclusion

In this tutorial, you learned how to manage administrative role assignments in Microsoft Entra ID by using PIM APIs. 
- While you made the group eligible for the administrative role, you can alternatively assign an active role to the group and make the members eligible to the group. In this scenario, use the PIM for groups APIs.
- The test user required MFA to activate their role. This requirement is part of the settings for the Microsoft Entra role and you can change the rules to not require MFA.
- As part of the configurable rules, you can also configure the following settings:
  - Limit the maximum allowed duration for the role activation.
  - Require or not require justification and ticket information for activating the role.

## Related content

+ [Tutorial: Assign Microsoft Entra roles in Privileged Identity Management using Microsoft Graph PowerShell](/powershell/microsoftgraph/tutorial-pim)
+ [Overview of role management through PIM](/graph/api/resources/privilegedidentitymanagementv3-overview)
+ [Govern membership and ownership of groups using PIM for groups](/graph/api/resources/privilegedidentitymanagement-for-groups-api-overview)
+ [Rules in PIM - mapping guide](/graph/identity-governance-pim-rules-overview)
