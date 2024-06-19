---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.users.item.messages.item.mark_as_junk.mark_as_junk_post_request_body import MarkAsJunkPostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = MarkAsJunkPostRequestBody(
	move_to_junk = True,
)

result = await graph_client.me.messages.by_message_id('message-id').mark_as_junk.post(request_body)


```