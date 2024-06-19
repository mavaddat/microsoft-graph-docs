---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.security.ediscovery_search import EdiscoverySearch

graph_client = GraphServiceClient(credentials, scopes)

request_body = EdiscoverySearch(
	display_name = "Teams search",
)

result = await graph_client.security.cases.ediscovery_cases.by_ediscovery_case_id('ediscoveryCase-id').searches.by_ediscovery_search_id('ediscoverySearch-id').patch(request_body)


```