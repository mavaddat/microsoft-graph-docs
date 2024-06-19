---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.message import Message

graph_client = GraphServiceClient(credentials, scopes)

request_body = Message(
	is_read = True,
)

result = await graph_client.me.messages.by_message_id('message-id').patch(request_body)


```