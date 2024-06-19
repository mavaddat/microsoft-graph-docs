---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.access_review_policy import AccessReviewPolicy

graph_client = GraphServiceClient(credentials, scopes)

request_body = AccessReviewPolicy(
	is_group_owner_management_enabled = True,
)

result = await graph_client.policies.access_review_policy.patch(request_body)


```