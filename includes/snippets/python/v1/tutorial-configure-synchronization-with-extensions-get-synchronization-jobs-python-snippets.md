---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.service_principals.item.synchronization.jobs.jobs_request_builder import JobsRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)


request_configuration = RequestConfiguration()
request_configuration.headers.add("Authorization", "Bearer {Token}")


result = await graph_client.service_principals.by_service_principal_id('servicePrincipal-id').synchronization.jobs.get(request_configuration = request_configuration)


```