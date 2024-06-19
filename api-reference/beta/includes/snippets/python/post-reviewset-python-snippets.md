---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.ediscovery.review_set import ReviewSet

graph_client = GraphServiceClient(credentials, scopes)

request_body = ReviewSet(
	display_name = "My Reviewset 3",
)

result = await graph_client.compliance.ediscovery.cases.by_case_id('case-id').review_sets.post(request_body)


```