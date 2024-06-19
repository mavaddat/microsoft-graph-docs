---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.identity_governance.role_management_alerts.alerts.item.unified_role_management_alert_item_request_builder import UnifiedRoleManagementAlertItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = UnifiedRoleManagementAlertItemRequestBuilder.UnifiedRoleManagementAlertItemRequestBuilderGetQueryParameters(
		expand = ["*"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity_governance.role_management_alerts.alerts.by_unified_role_management_alert_id('unifiedRoleManagementAlert-id').get(request_configuration = request_configuration)


```