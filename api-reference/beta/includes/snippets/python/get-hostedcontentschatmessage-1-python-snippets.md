---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.chats.by_chat_id('chat-id').messages.by_chat_message_id('chatMessage-id').hosted_contents.get()


```