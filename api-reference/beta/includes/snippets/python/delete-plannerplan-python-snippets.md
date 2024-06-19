---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.planner.plans.item.planner_plan_item_request_builder import PlannerPlanItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)


request_configuration = RequestConfiguration()
request_configuration.headers.add("If-Match", "W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc=\"")


await graph_client.planner.plans.by_planner_plan_id('plannerPlan-id').delete(request_configuration = request_configuration)


```