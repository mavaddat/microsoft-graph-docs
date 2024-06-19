---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.sites.get_all_sites.get_all_sites_request_builder import GetAllSitesRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = GetAllSitesRequestBuilder.GetAllSitesRequestBuilderGetQueryParameters(
		skiptoken = "U1BHZW9EYXRhTG9jYXRpb25Db2RlYU5BTQ",
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.sites.get_all_sites.get(request_configuration = request_configuration)


```