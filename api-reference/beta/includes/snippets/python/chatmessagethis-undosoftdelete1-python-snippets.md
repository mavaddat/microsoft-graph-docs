---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.users.by_user_id('user-id').chats.by_chat_id('chat-id').messages.by_chat_message_id('chatMessage-id').undo_soft_delete.post()


```