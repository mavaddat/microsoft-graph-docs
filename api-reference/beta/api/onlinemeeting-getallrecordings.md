---
title: "onlineMeeting: getAllRecordings"
description: "Get recordings from all online meetings that a user is an organizer of."
author: "suvanka"
ms.localizationpriority: medium
ms.subservice: "teams"
doc_type: apiPageType
---

# onlineMeeting: getAllRecordings

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get all recordings from scheduled [onlineMeeting](../resources/onlinemeeting.md) instances for which the specified user is the organizer. This API currently doesn't support getting call recordings from channel meetings.

You can apply the [delta](callrecording-delta.md) function on **getAllRecordings** to synchronize and get [callRecording](../resources/callrecording.md) resources as they're added for **onlineMeeting** instances organized by the specified user.

The delta query supports both full synchronization and incremental synchronization. Full synchronization gets all the recordings for online meetings organized by the user. Incremental synchronization gets recordings that are added since the last synchronization. Typically, you would do an initial full synchronization, and then get incremental changes to that recording view periodically.

Find more information in the [delta query](/graph/delta-query-overview) documentation. For more examples, see [callRecording: delta](callrecording-delta.md).

To learn more about using the Microsoft Teams export APIs to export content, see [Export content with the Microsoft Teams export APIs](/microsoftteams/export-teams-content).

[!INCLUDE [national-cloud-support](../../includes/global-only.md)]

### Known issues

The following known issues are associated with this API:

- [Using the `$top` query parameter might not return the @odata.nextLink](https://developer.microsoft.com/en-us/graph/known-issues/?search=22931).
- [Recordings aren't exported for meetings that don't have transcription turned on](https://developer.microsoft.com/en-us/graph/known-issues/?search=22933).

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "onlinemeeting_getallrecordings" } -->
[!INCLUDE [permissions-table](../includes/permissions/onlinemeeting-getallrecordings-permissions.md)]

## HTTP request

<!-- { "blockType": "ignored" } -->
``` http
GET /users/{usersId}/onlineMeetings/getAllRecordings(meetingOrganizerUserId='{userId}',startDateTime={startDateTime},endDateTime={endDateTime})
```
>**Note:** If you don't pass the function parameter **meetingOrganizerUserId**, the request fails.

## Function parameters
In the request URL, provide the following query parameters with values.

|Parameter|Type|Description|
|:---|:---|:---|
|meetingOrganizerUserId|String|The user identifier of the meeting organizer to filter for artifacts for meetings organized by the given user identifier.|
|startDateTime|DateTimeOffset|Optional parameter to filter for artifacts created after the given start date.|
|endDateTime|DateTimeOffset|Optional parameter to filter for artifacts created before the given end date.|

## Supported query patterns

| Pattern                | Supported | Syntax                                                  | Notes                                                                                                        |
| ---------------------- | :-------: | ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Page size              |     ✓     | `top`                                                   | Allows caller to specify max number of objects per page. |

## Request headers

| Header       | Value |
|:---------------|:--------|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Response

If successful, this method returns a `200 OK` response code and a list of [callRecording](../resources/callrecording.md) objects in the response body.

## Examples

### Example 1: Get all recordings

The following example shows a request to get all the recordings of a given meeting organizer.

#### Request

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "sampleKeys": ["8b081ef6-4792-4def-b2c9-c363a1bf41d5"],
  "name": "get_allrecordings"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/users/8b081ef6-4792-4def-b2c9-c363a1bf41d5/onlineMeetings/getAllRecordings(meetingOrganizerUserId='8b081ef6-4792-4def-b2c9-c363a1bf41d5')
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-allrecordings-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/get-allrecordings-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/get-allrecordings-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [snippet-not-available](../includes/snippets/snippet-not-available.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-allrecordings-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [snippet-not-available](../includes/snippets/snippet-not-available.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [snippet-not-available](../includes/snippets/snippet-not-available.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [snippet-not-available](../includes/snippets/snippet-not-available.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

---

#### Response

>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "name": "get_allrecordings",
  "@odata.type": "microsoft.graph.callRecording",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(callRecording)",
    "@odata.nextLink": "https://graph.microsoft.com/beta/users({userId})/onlineMeetings/getAllRecordings(meetingOrganizerUserId='8b081ef6-4792-4def-b2c9-c363a1bf41d5')?skipToken={skipToken}",
    "@odata.count": 1,
    "value": [
        {
            "@odata.type": "#microsoft.graph.callRecording",
            "id": "VjIjIzExYzkxNjVmZi1hZTkyLTQ5YWYtODliNC00MTU1NTRhMzZhNTFhMWQyODZkYi02MTQ5LTRiM2QtOTVhZC0yM2M5ZTFiZjY4NTMwNDAwMDAwMDgyMDBFMDAwNzRDNUI3MTAxQTgyRTAwODA3ZTcwYzAyM2U4MGEwOWVmN2ZmZDkwMTAwMDAwMDAwMDAwMDAwMDAxMDAwMDAwMDI3N2Q3NzZjYmNmMjQ5NGNiNDk0NDExZGE3YzRhMmM1IyM3YTM2NDRjYi1mMDA3LTRjMDAtOWJiMy1jMTUzYzE4ODY4NGY=",
            "meetingId": "MSoxYzkxNjVmZi1hZTkyLTQ5YWYtODliNC00MTU1NTRhMzZhNTEqMCoqMTk6bWVldGluZ19PVEJsT1RjeE16QXROemMwWVMwMFl6QTFMVGhpWldFdFpUaGtNMlk0WkRKaFlUQTFAdGhyZWFkLnYy",
            "meetingOrganizerId": "8b081ef6-4792-4def-b2c9-c363a1bf41d5",
            "createdDateTime": "2023-12-02T06:59:34.7411768Z",
            "recordingContentUrl": "https://graph.microsoft.com/beta/users/8b081ef6-4792-4def-b2c9-c363a1bf41d5/onlineMeetings/MSoxYzkxNjVmZi1hZTkyLTQ5YWYtODliNC00MTU1NTRhMzZhNTEqMCoqMTk6bWVldGluZ19PVEJsT1RjeE16QXROemMwWVMwMFl6QTFMVGhpWldFdFpUaGtNMlk0WkRKaFlUQTFAdGhyZWFkLnYy/recordings/VjIjIzExYzkxNjVmZi1hZTkyLTQ5YWYtODliNC00MTU1NTRhMzZhNTFhMWQyODZkYi02MTQ5LTRiM2QtOTVhZC0yM2M5ZTFiZjY4NTMwNDAwMDAwMDgyMDBFMDAwNzRDNUI3MTAxQTgyRTAwODA3ZTcwYzAyM2U4MGEwOWVmN2ZmZDkwMTAwMDAwMDAwMDAwMDAwMDAxMDAwMDAwMDI3N2Q3NzZjYmNmMjQ5NGNiNDk0NDExZGE3YzRhMmM1IyM3YTM2NDRjYi1mMDA3LTRjMDAtOWJiMy1jMTUzYzE4ODY4NGY=/content",
            "meetingOrganizer": {
                "application": null,
                "device": null,
                "user": {
                    "@odata.type": "#microsoft.graph.teamworkUserIdentity",
                    "id": "8b081ef6-4792-4def-b2c9-c363a1bf41d5",
                    "displayName": null,
                    "userIdentityType": "aadUser",
                    "tenantId": "a1d286db-6149-4b3d-95ad-23c9e1bf6853"
                }
            }          
        }
    ]
}
```

### Example 2: Get all recordings of a given meeting organizer with date range filter

The following example shows a request to get all recordings of a given meeting organizer, that are created between a given start date and an end date.

#### Request

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "sampleKeys": ["8b081ef6-4792-4def-b2c9-c363a1bf41d5", "2024-01-15T00:00:00Z", "2024-01-31T00:00:00Z"],
  "name": "get_allrecordings_with_dates"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/users/8b081ef6-4792-4def-b2c9-c363a1bf41d5/onlineMeetings/getAllRecordings(meetingOrganizerUserId='8b081ef6-4792-4def-b2c9-c363a1bf41d5', startDateTime=2024-01-15T00:00:00Z, endDateTime=2024-01-31T00:00:00Z)
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-allrecordings-with-dates-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/get-allrecordings-with-dates-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/get-allrecordings-with-dates-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-allrecordings-with-dates-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-allrecordings-with-dates-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/get-allrecordings-with-dates-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/get-allrecordings-with-dates-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/get-allrecordings-with-dates-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

---

#### Response

>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "name": "get_allrecordings_with_dates",
  "@odata.type": "microsoft.graph.callRecording",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(callRecording)",
    "@odata.nextLink": "https://graph.microsoft.com/beta/users({userId})/onlineMeetings/getAllRecordings(meetingOrganizerUserId='8b081ef6-4792-4def-b2c9-c363a1bf41d5', startDateTime=2024-01-15T00:00:00Z, endDateTime=2024-01-31T00:00:00Z)?skipToken={skipToken}",
    "@odata.count": 1,
    "value": [
        {
            "@odata.type": "#microsoft.graph.callRecording",
            "id": "VjIjIzExYzkxNjVmZi1hZTkyLTQ5YWYtODliNC00MTU1NTRhMzZhNTFhMWQyODZkYi02MTQ5LTRiM2QtOTVhZC0yM2M5ZTFiZjY4NTMwNDAwMDAwMDgyMDBFMDAwNzRDNUI3MTAxQTgyRTAwODA3ZTcwYzAyM2U4MGEwOWVmN2ZmZDkwMTAwMDAwMDAwMDAwMDAwMDAxMDAwMDAwMDI3N2Q3NzZjYmNmMjQ5NGNiNDk0NDExZGE3YzRhMmM1IyM3YTM2NDRjYi1mMDA3LTRjMDAtOWJiMy1jMTUzYzE4ODY4NGY=",
            "meetingId": "MSoxYzkxNjVmZi1hZTkyLTQ5YWYtODliNC00MTU1NTRhMzZhNTEqMCoqMTk6bWVldGluZ19PVEJsT1RjeE16QXROemMwWVMwMFl6QTFMVGhpWldFdFpUaGtNMlk0WkRKaFlUQTFAdGhyZWFkLnYy",
            "meetingOrganizerId": "8b081ef6-4792-4def-b2c9-c363a1bf41d5",
            "createdDateTime": "2023-12-02T06:59:34.7411768Z",
            "recordingContentUrl": "https://graph.microsoft.com/beta/users/8b081ef6-4792-4def-b2c9-c363a1bf41d5/onlineMeetings/MSoxYzkxNjVmZi1hZTkyLTQ5YWYtODliNC00MTU1NTRhMzZhNTEqMCoqMTk6bWVldGluZ19PVEJsT1RjeE16QXROemMwWVMwMFl6QTFMVGhpWldFdFpUaGtNMlk0WkRKaFlUQTFAdGhyZWFkLnYy/recordings/VjIjIzExYzkxNjVmZi1hZTkyLTQ5YWYtODliNC00MTU1NTRhMzZhNTFhMWQyODZkYi02MTQ5LTRiM2QtOTVhZC0yM2M5ZTFiZjY4NTMwNDAwMDAwMDgyMDBFMDAwNzRDNUI3MTAxQTgyRTAwODA3ZTcwYzAyM2U4MGEwOWVmN2ZmZDkwMTAwMDAwMDAwMDAwMDAwMDAxMDAwMDAwMDI3N2Q3NzZjYmNmMjQ5NGNiNDk0NDExZGE3YzRhMmM1IyM3YTM2NDRjYi1mMDA3LTRjMDAtOWJiMy1jMTUzYzE4ODY4NGY=/content",
            "meetingOrganizer": {
                "application": null,
                "device": null,
                "user": {
                    "@odata.type": "#microsoft.graph.teamworkUserIdentity",
                    "id": "8b081ef6-4792-4def-b2c9-c363a1bf41d5",
                    "displayName": null,
                    "userIdentityType": "aadUser",
                    "tenantId": "a1d286db-6149-4b3d-95ad-23c9e1bf6853"
                }
            }          
        }
    ]
}
```

## Related content

[Microsoft Graph service-specific throttling limits](/graph/throttling-limits#microsoft-teams-service-limits)

[Delta query overview](/graph/delta-query-overview)

[Export content with the Microsoft Teams export APIs](/microsoftteams/export-teams-content)
