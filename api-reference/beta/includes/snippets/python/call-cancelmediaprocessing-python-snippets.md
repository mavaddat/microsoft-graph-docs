---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.communications.calls.item.cancel_media_processing.cancel_media_processing_post_request_body import CancelMediaProcessingPostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = CancelMediaProcessingPostRequestBody(
	client_context = "clientContext-value",
)

result = await graph_client.communications.calls.by_call_id('call-id').cancel_media_processing.post(request_body)


```