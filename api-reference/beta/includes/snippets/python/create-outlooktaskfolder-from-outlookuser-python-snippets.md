---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.outlook_task_folder import OutlookTaskFolder

graph_client = GraphServiceClient(credentials, scopes)

request_body = OutlookTaskFolder(
	name = "Volunteer",
)

result = await graph_client.me.outlook.task_folders.post(request_body)


```