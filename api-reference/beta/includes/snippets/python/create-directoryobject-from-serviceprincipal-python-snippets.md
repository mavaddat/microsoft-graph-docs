---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.reference_create import ReferenceCreate

graph_client = GraphServiceClient(credentials, scopes)

request_body = ReferenceCreate(
	odata_id = "https://graph.microsoft.com/v1.0/directoryObjects/{id}",
)

await graph_client.service_principals.by_service_principal_id('servicePrincipal-id').owners.ref.post(request_body)


```