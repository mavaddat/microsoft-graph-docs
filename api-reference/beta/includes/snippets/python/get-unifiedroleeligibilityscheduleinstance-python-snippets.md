---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.role_management.directory.role_eligibility_schedule_instances.by_unified_role_eligibility_schedule_instance_id('unifiedRoleEligibilityScheduleInstance-id').get()


```