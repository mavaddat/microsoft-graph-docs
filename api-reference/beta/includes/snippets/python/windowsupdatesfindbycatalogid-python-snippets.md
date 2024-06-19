---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.admin.windows.updates.products.microsoft.graph.windows_updates.find_by_kb_number(kb_number={kb_number}).find_by_kb_number_with_kb_number_request_builder import FindByKbNumberWithKbNumberRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = FindByKbNumberWithKbNumberRequestBuilder.FindByKbNumberWithKbNumberRequestBuilderGetQueryParameters(
		expand = ["revisions($expand=catalogEntry,knowledgeBaseArticle)","knownIssues"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.admin.windows.updates.products.microsoft_graph_windows_updates_find_by_kb_number_with_kb_number(1).get(request_configuration = request_configuration)


```