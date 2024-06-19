---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.communications.calls.item.reject.reject_post_request_body import RejectPostRequestBody
from msgraph.generated.models.reject_reason import RejectReason

graph_client = GraphServiceClient(credentials, scopes)

request_body = RejectPostRequestBody(
	reason = RejectReason.Busy,
)

await graph_client.communications.calls.by_call_id('call-id').reject.post(request_body)


```