---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.external_connectors.external_connection import ExternalConnection

graph_client = GraphServiceClient(credentials, scopes)

request_body = ExternalConnection(
	id = "contosohr",
	name = "Contoso HR",
	description = "Connection to index Contoso HR system",
)

result = await graph_client.external.connections.post(request_body)


```