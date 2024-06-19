---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.entitlement_management_settings import EntitlementManagementSettings

graph_client = GraphServiceClient(credentials, scopes)

request_body = EntitlementManagementSettings(
	external_user_lifecycle_action = "None",
)

result = await graph_client.identity_governance.entitlement_management.settings.patch(request_body)


```