---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.role_management.device_management.role_assignments.item.unified_role_assignment_multiple_item_request_builder import UnifiedRoleAssignmentMultipleItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = UnifiedRoleAssignmentMultipleItemRequestBuilder.UnifiedRoleAssignmentMultipleItemRequestBuilderGetQueryParameters(
		expand = ["roleDefinition","principals","directoryScopes"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.role_management.device_management.role_assignments.by_unified_role_assignment_multiple_id('unifiedRoleAssignmentMultiple-id').get(request_configuration = request_configuration)


```