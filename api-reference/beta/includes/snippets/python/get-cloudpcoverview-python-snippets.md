---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.tenant_relationships.managed_tenants.cloud_pcs_overview.by_cloud_pc_overview_tenant_id('cloudPcOverview-tenantId').get()


```