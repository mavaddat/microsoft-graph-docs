---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.security.attack_simulation.landing_pages.landing_pages_request_builder import LandingPagesRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = LandingPagesRequestBuilder.LandingPagesRequestBuilderGetQueryParameters(
		filter = "source eq 'tenant'",
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.security.attack_simulation.landing_pages.get(request_configuration = request_configuration)


```