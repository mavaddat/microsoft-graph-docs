---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.policies.feature_rollout_policies.item.feature_rollout_policy_item_request_builder import FeatureRolloutPolicyItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = FeatureRolloutPolicyItemRequestBuilder.FeatureRolloutPolicyItemRequestBuilderGetQueryParameters(
		expand = ["appliesTo"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.policies.feature_rollout_policies.by_feature_rollout_policy_id('featureRolloutPolicy-id').get(request_configuration = request_configuration)


```