---
title: "virtualEventWebinar resource type"
description: "Contains information about a virtual event webinar."
author: "awang119"
ms.localizationpriority: medium
ms.subservice: "cloud-communications"
doc_type: resourcePageType
---

# virtualEventWebinar resource type

Namespace: microsoft.graph

Contains information about a virtual event webinar.

Inherits from [virtualEvent](../resources/virtualevent.md).

## Methods

| Method | Return Type |Description |
| ------ | ----------- | ---------- |
| [List](../api/virtualeventsroot-list-webinars.md) | [virtualEventWebinar](../resources/virtualeventwebinar.md) collection | Get the list of all [virtualEventWebinar](../resources/virtualeventwebinar.md) objects created in the tenant. |
| [Get](../api/virtualeventwebinar-get.md) | [virtualEventWebinar](../resources/virtualeventwebinar.md) | Read the properties and relationships of a [virtualEventWebinar](../resources/virtualeventwebinar.md) object. |
| [List by user role](../api/virtualeventwebinar-getbyuserrole.md) | [virtualEventWebinar](../resources/virtualeventwebinar.md) collection | Get a **virtualEventWebinar** collection where the signed-in user is either the organizer or a co-organizer. |
| [List by user ID and role](../api/virtualeventwebinar-getbyuseridandrole.md) | [virtualEventWebinar](../resources/virtualeventwebinar.md) collection | Get a **virtualEventWebinar** collection where the specified user is either the organizer or a co-organizer. |

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| audience | [meetingAudience](#meetingaudience-values) | To whom the webinar is visible. |
| coOrganizers  | [communicationsUserIdentity](communicationsuseridentity.md) collection | Identity information of coorganizers of the webinar. |
| createdBy | [communicationsIdentitySet](communicationsidentityset.md) | Identity information for the creator of the webinar. Inherited from [virtualEvent](../resources/virtualevent.md). |
| description | [itemBody](../resources/itembody.md) | Description of the webinar. Inherited from [virtualEvent](../resources/virtualevent.md). |
| displayName | String | Display name of the webinar. Inherited from [virtualEvent](../resources/virtualevent.md). |
| endDateTime | [dateTimeTimeZone](../resources/datetimetimezone.md) | End time of the webinar. The **timeZone** property _can_ be set to any of the time zones currently supported by Windows. For details on how to get all available time zones using PowerShell, see [Get-TimeZone](/powershell/module/microsoft.powershell.management/get-timezone#example-3-get-all-available-time-zones).|
| startDateTime | [dateTimeTimeZone](../resources/datetimetimezone.md) | Start time of the webinar. The **timeZone** property _can_ be set to any of the time zones currently supported by Windows. For details on how to get all available time zones using PowerShell, see [Get-TimeZone](/powershell/module/microsoft.powershell.management/get-timezone#example-3-get-all-available-time-zones).|
| id | String | Unique identifier of the webinar. Inherited from [entity](../resources/entity.md).|
| status | [virtualEventStatus](#virtualeventstatus-values) | Status of the webinar. |

### meetingAudience values

| Value | Description |
| ----- | ----------- |
| everyone | The webinar is a public webinar. A public webinar is visible to everyone. |
| organization | The webinar is a private webinar. A private webinar is visible only within the same organization as the organizer. |
| unknownFutureValue | Evolvable enumeration sentinel value. Don't use. |

### virtualEventStatus values

| Value | Description |
| ----- | ----------- |
| draft | The webinar is in draft and only visible to the organizer. |
| published | The organizer published the webinar and it's visible to the audience. |
| canceled | The organizer canceled the webinar. |
| unknownFutureValue | Evolvable enumeration sentinel value. Don't use. |

## Relationships

| Relationship | Type | Description |
| ------------ | ---- | ----------- |
| registrations | [virtualEventRegistration](../resources/virtualeventregistration.md) collection | Registration records of the webinar. |
| sessions | [virtualEventSession](../resources/virtualeventsession.md)  collection | Sessions of the webinar. Inherited from [virtualEvent](../resources/virtualevent.md). |

## JSON representation
The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.virtualEventWebinar",
  "baseType": "microsoft.graph.virtualEvent",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.virtualEventWebinar",
  "id": "String (identifier)",
  "status": "String",
  "displayName": "String",
  "description": {
    "@odata.type": "microsoft.graph.itemBody"
  },
  "startDateTime": {
    "@odata.type": "microsoft.graph.dateTimeTimeZone"
  },
  "endDateTime": {
    "@odata.type": "microsoft.graph.dateTimeTimeZone"
  },
  "createdBy": {
    "@odata.type": "microsoft.graph.communicationsIdentitySet"
  },
  "audience": "String",
  "coOrganizers": [
    {
      "@odata.type": "microsoft.graph.communicationsUserIdentity"
    }
  ]
}
```

## Related content

[List meetingAttendanceReports](../api/meetingattendancereport-list.md)