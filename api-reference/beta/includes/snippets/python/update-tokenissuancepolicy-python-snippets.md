---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.token_issuance_policy import TokenIssuancePolicy

graph_client = GraphServiceClient(credentials, scopes)

request_body = TokenIssuancePolicy(
	definition = [
		"definition-value",
	],
	display_name = "displayName-value",
	is_organization_default = True,
)

result = await graph_client.policies.token_issuance_policies.by_token_issuance_policy_id('tokenIssuancePolicy-id').patch(request_body)


```