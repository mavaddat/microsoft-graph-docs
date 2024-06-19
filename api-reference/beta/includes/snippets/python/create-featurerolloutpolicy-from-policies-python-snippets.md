---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.feature_rollout_policy import FeatureRolloutPolicy
from msgraph_beta.generated.models.staged_feature_name import StagedFeatureName

graph_client = GraphServiceClient(credentials, scopes)

request_body = FeatureRolloutPolicy(
	display_name = "PassthroughAuthentication rollout policy",
	description = "PassthroughAuthentication rollout policy",
	feature = StagedFeatureName.PassthroughAuthentication,
	is_enabled = True,
	is_applied_to_organization = False,
)

result = await graph_client.policies.feature_rollout_policies.post(request_body)


```