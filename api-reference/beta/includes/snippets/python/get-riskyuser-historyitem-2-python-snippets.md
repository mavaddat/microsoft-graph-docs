---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.identity_protection.risky_users.by_risky_user_id('riskyUser-id').history.by_risky_user_history_item_id('riskyUserHistoryItem-id').get()


```