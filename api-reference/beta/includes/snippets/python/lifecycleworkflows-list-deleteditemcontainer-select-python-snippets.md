---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.identity_governance.lifecycle_workflows.deleted_items.workflows.workflows_request_builder import WorkflowsRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = WorkflowsRequestBuilder.WorkflowsRequestBuilderGetQueryParameters(
		select = ["id","category","displayName","description","version"],
		filter = "category eq 'leaver'",
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity_governance.lifecycle_workflows.deleted_items.workflows.get(request_configuration = request_configuration)


```