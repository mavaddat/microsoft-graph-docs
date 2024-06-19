---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.sites.item.lists.item.list_item_request_builder import ListItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = ListItemRequestBuilder.ListItemRequestBuilderGetQueryParameters(
		select = ["id","name","lastModifiedDateTime"],
		expand = ["columns(select=name,description)","items(expand=fields(select=Name,Color,Quantity)",")"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.sites.by_site_id('site-id').lists.by_list_id('list-id').get(request_configuration = request_configuration)


```