---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.teamwork.devices.item.update_software.update_software_post_request_body import UpdateSoftwarePostRequestBody
from msgraph_beta.generated.models.teamwork_software_type import TeamworkSoftwareType

graph_client = GraphServiceClient(credentials, scopes)

request_body = UpdateSoftwarePostRequestBody(
	software_type = TeamworkSoftwareType.TeamsClient,
	software_version = "1.0.96.22",
)

await graph_client.teamwork.devices.by_teamwork_device_id('teamworkDevice-id').update_software.post(request_body)


```