---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.communications.calls.item.unmute.unmute_post_request_body import UnmutePostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = UnmutePostRequestBody(
	client_context = "clientContext-value",
)

result = await graph_client.communications.calls.by_call_id('call-id').unmute.post(request_body)


```