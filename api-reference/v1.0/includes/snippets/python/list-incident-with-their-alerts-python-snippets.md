---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.security.incidents.incidents_request_builder import IncidentsRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = IncidentsRequestBuilder.IncidentsRequestBuilderGetQueryParameters(
		expand = ["alerts"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.security.incidents.get(request_configuration = request_configuration)


```