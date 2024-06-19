---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.security.cases.ediscovery_cases.item.noncustodial_data_sources.noncustodial_data_sources_request_builder import NoncustodialDataSourcesRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = NoncustodialDataSourcesRequestBuilder.NoncustodialDataSourcesRequestBuilderGetQueryParameters(
		expand = ["dataSource"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.security.cases.ediscovery_cases.by_ediscovery_case_id('ediscoveryCase-id').noncustodial_data_sources.get(request_configuration = request_configuration)


```