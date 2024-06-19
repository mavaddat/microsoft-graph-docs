---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.todo_task_list import TodoTaskList

graph_client = GraphServiceClient(credentials, scopes)

request_body = TodoTaskList(
	display_name = "Travel items",
)

result = await graph_client.me.todo.lists.post(request_body)


```