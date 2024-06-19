---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.identity_governance.lifecycle_workflows.workflow_templates.workflow_templates_request_builder import WorkflowTemplatesRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = WorkflowTemplatesRequestBuilder.WorkflowTemplatesRequestBuilderGetQueryParameters(
		filter = "category eq 'leaver'",
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity_governance.lifecycle_workflows.workflow_templates.get(request_configuration = request_configuration)


```