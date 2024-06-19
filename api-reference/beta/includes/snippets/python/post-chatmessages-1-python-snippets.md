---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.chat_message import ChatMessage
from msgraph_beta.generated.models.item_body import ItemBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = ChatMessage(
	body = ItemBody(
		content = "Hello world",
	),
)

result = await graph_client.chats.by_chat_id('chat-id').messages.post(request_body)


```