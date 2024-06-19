---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.windows_updates.update_policy import UpdatePolicy
from msgraph_beta.generated.models.windows_updates.deployment_settings import DeploymentSettings
from msgraph_beta.generated.models.windows_updates.schedule_settings import ScheduleSettings
from msgraph_beta.generated.models.windows_updates.rate_driven_rollout_settings import RateDrivenRolloutSettings

graph_client = GraphServiceClient(credentials, scopes)

request_body = UpdatePolicy(
	odata_type = "#microsoft.graph.windowsUpdates.updatePolicy",
	deployment_settings = DeploymentSettings(
		odata_type = "microsoft.graph.windowsUpdates.deploymentSettings",
		schedule = ScheduleSettings(
			gradual_rollout = RateDrivenRolloutSettings(
				odata_type = "#microsoft.graph.windowsUpdates.rateDrivenRolloutSettings",
				duration_between_offers = "P1D",
				additional_data = {
						"device_per_offer" : 1000,
				}
			),
		),
	),
)

result = await graph_client.admin.windows.updates.update_policies.by_update_policy_id('updatePolicy-id').patch(request_body)


```