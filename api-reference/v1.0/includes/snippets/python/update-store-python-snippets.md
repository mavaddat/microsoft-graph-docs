---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.models.term_store.store import Store

graph_client = GraphServiceClient(credentials, scopes)

request_body = Store(
	default_language_tag = "en-US",
)

result = await graph_client.sites.by_site_id('site-id').term_store.patch(request_body)


```