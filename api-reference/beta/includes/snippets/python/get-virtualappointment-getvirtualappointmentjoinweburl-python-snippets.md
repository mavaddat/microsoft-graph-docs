---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.me.online_meetings.by_online_meeting_id('onlineMeeting-id').get_virtual_appointment_join_web_url.get()


```