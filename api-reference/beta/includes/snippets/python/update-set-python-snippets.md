---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.term_store.set import Set

graph_client = GraphServiceClient(credentials, scopes)

request_body = Set(
	description = "mySet",
)

result = await graph_client.term_store.sets.by_set_id('set-id').patch(request_body)


```