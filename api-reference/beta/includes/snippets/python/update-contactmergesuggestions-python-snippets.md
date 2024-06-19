---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.contact_merge_suggestions import ContactMergeSuggestions

graph_client = GraphServiceClient(credentials, scopes)

request_body = ContactMergeSuggestions(
	is_enabled = False,
)

result = await graph_client.me.settings.contact_merge_suggestions.patch(request_body)


```