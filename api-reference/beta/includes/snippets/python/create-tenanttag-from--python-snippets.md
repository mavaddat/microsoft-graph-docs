---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.managed_tenants.tenant_tag import TenantTag

graph_client = GraphServiceClient(credentials, scopes)

request_body = TenantTag(
	display_name = "Support",
	description = "Tenants that have purchased extended support",
)

result = await graph_client.tenant_relationships.managed_tenants.tenant_tags.post(request_body)


```