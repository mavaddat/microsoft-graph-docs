---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.sites.item.pages.item.graph.site_page.site_page_request_builder import SitePageRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = SitePageRequestBuilder.SitePageRequestBuilderGetQueryParameters(
		select = ["id","name"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.sites.by_site_id('site-id').pages.by_base_site_page_id('baseSitePage-id').graph_site_page.get(request_configuration = request_configuration)


```