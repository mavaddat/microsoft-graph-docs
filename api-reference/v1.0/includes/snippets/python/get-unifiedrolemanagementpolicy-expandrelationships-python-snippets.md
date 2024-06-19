---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.policies.role_management_policies.item.unified_role_management_policy_item_request_builder import UnifiedRoleManagementPolicyItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = UnifiedRoleManagementPolicyItemRequestBuilder.UnifiedRoleManagementPolicyItemRequestBuilderGetQueryParameters(
		expand = ["effectiveRules","rules"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.policies.role_management_policies.by_unified_role_management_policy_id('unifiedRoleManagementPolicy-id').get(request_configuration = request_configuration)


```