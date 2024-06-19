---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.chat import Chat

graph_client = GraphServiceClient(credentials, scopes)

request_body = Chat(
	topic = "Group chat title update",
)

result = await graph_client.chats.by_chat_id('chat-id').patch(request_body)


```