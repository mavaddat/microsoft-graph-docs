---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.planner.rosters.by_planner_roster_id('plannerRoster-id').plans.by_planner_plan_id('plannerPlan-id').get()


```