---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.teams.by_team_id('team-id').schedule.times_off.by_time_off_id('timeOff-id').delete()


```