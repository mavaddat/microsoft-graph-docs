---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.onenote_section import OnenoteSection

graph_client = GraphServiceClient(credentials, scopes)

request_body = OnenoteSection(
	display_name = "Section name",
)

result = await graph_client.me.onenote.notebooks.by_notebook_id('notebook-id').sections.post(request_body)


```