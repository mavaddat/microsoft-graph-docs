---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.external_identities_policy import ExternalIdentitiesPolicy

graph_client = GraphServiceClient(credentials, scopes)

request_body = ExternalIdentitiesPolicy(
	allow_external_identities_to_leave = False,
)

result = await graph_client.policies.external_identities_policy.patch(request_body)


```