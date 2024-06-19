---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.role_management.directory.resource_namespaces.item.resource_actions.resource_actions_request_builder import ResourceActionsRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = ResourceActionsRequestBuilder.ResourceActionsRequestBuilderGetQueryParameters(
		filter = "isPrivileged eq true",
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.role_management.directory.resource_namespaces.by_unified_rbac_resource_namespace_id('unifiedRbacResourceNamespace-id').resource_actions.get(request_configuration = request_configuration)


```