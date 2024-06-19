---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.notebook import Notebook

graph_client = GraphServiceClient(credentials, scopes)

request_body = Notebook(
	display_name = "My Private notebook",
)

result = await graph_client.me.onenote.notebooks.post(request_body)


```