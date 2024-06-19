---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.models.reference_create import ReferenceCreate

graph_client = GraphServiceClient(credentials, scopes)

request_body = ReferenceCreate(
	odata_id = "https://graph.microsoft.com/v1.0/groups/{id}",
)

await graph_client.directory.administrative_units.by_administrative_unit_id('administrativeUnit-id').members.ref.post(request_body)


```