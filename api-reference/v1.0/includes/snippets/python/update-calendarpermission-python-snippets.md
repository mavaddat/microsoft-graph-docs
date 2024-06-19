---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.models.calendar_permission import CalendarPermission
from msgraph.generated.models.calendar_role_type import CalendarRoleType

graph_client = GraphServiceClient(credentials, scopes)

request_body = CalendarPermission(
	role = CalendarRoleType.Write,
)

result = await graph_client.users.by_user_id('user-id').calendar.calendar_permissions.by_calendar_permission_id('calendarPermission-id').patch(request_body)


```