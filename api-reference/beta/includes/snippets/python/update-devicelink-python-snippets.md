---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.networkaccess.device_link import DeviceLink

graph_client = GraphServiceClient(credentials, scopes)

request_body = DeviceLink(
	name = "Backup Link",
)

result = await graph_client.network_access.connectivity.branches.by_branch_site_id('branchSite-id').device_links.by_device_link_id('deviceLink-id').patch(request_body)


```