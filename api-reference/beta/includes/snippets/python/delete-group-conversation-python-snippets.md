---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.groups.by_group_id('group-id').conversations.by_conversation_id('conversation-id').delete()


```