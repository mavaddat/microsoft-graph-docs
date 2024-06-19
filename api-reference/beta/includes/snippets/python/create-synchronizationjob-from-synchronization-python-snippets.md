---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.synchronization_job import SynchronizationJob

graph_client = GraphServiceClient(credentials, scopes)

request_body = SynchronizationJob(
	template_id = "BoxOutDelta",
)

result = await graph_client.service_principals.by_service_principal_id('servicePrincipal-id').synchronization.jobs.post(request_body)


```