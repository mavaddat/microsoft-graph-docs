---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.security.cases.ediscovery_cases.item.noncustodial_data_sources.item.ediscovery_noncustodial_data_source_item_request_builder import EdiscoveryNoncustodialDataSourceItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = EdiscoveryNoncustodialDataSourceItemRequestBuilder.EdiscoveryNoncustodialDataSourceItemRequestBuilderGetQueryParameters(
		expand = ["dataSource"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.security.cases.ediscovery_cases.by_ediscovery_case_id('ediscoveryCase-id').noncustodial_data_sources.by_ediscovery_noncustodial_data_source_id('ediscoveryNoncustodialDataSource-id').get(request_configuration = request_configuration)


```