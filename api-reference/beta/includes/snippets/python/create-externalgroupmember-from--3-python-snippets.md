---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.external_connectors.identity import Identity
from msgraph_beta.generated.models.identity_type import IdentityType

graph_client = GraphServiceClient(credentials, scopes)

request_body = Identity(
	id = "1431b9c38ee647f6a",
	type = IdentityType.ExternalGroup,
)

result = await graph_client.external.connections.by_external_connection_id('externalConnection-id').groups.by_external_group_id('externalGroup-id').members.post(request_body)


```