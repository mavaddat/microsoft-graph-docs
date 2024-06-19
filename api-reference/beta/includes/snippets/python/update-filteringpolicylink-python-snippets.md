---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.networkaccess.filtering_policy_link import FilteringPolicyLink
from msgraph_beta.generated.models.status import Status

graph_client = GraphServiceClient(credentials, scopes)

request_body = FilteringPolicyLink(
	odata_type = "#microsoft.graph.networkaccess.filteringPolicyLink",
	state = Status.Disabled,
)

result = await graph_client.network_access.filtering_profiles.by_filtering_profile_id('filteringProfile-id').policies.by_policy_link_id('policyLink-id').patch(request_body)


```