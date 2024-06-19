---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.security.ediscovery_case import EdiscoveryCase

graph_client = GraphServiceClient(credentials, scopes)

request_body = EdiscoveryCase(
	display_name = "My Case 1 - Renamed",
	description = "Updated description",
)

result = await graph_client.security.cases.ediscovery_cases.by_ediscovery_case_id('ediscoveryCase-id').patch(request_body)


```