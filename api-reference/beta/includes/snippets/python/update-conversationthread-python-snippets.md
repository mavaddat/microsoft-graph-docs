---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.conversation_thread import ConversationThread

graph_client = GraphServiceClient(credentials, scopes)

request_body = ConversationThread(
	is_locked = True,
)

result = await graph_client.groups.by_group_id('group-id').threads.by_conversation_thread_id('conversationThread-id').patch(request_body)


```