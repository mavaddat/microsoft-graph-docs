---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.models.external_connectors.identity import Identity
from msgraph.generated.models.identity_type import IdentityType

graph_client = GraphServiceClient(credentials, scopes)

request_body = Identity(
	id = "e5477431-1038-484e-bf69-1dfedb97a110",
	type = IdentityType.Group,
)

result = await graph_client.external.connections.by_external_connection_id('externalConnection-id').groups.by_external_group_id('externalGroup-id').members.post(request_body)


```