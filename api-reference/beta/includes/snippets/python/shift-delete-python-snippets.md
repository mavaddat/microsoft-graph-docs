---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.teams.by_team_id('team-id').schedule.shifts.by_shift_id('shift-id').delete()


```