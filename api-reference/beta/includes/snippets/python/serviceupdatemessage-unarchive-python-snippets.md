---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.admin.serviceannouncement.messages.unarchive.unarchive_post_request_body import UnarchivePostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = UnarchivePostRequestBody(
	message_ids = [
		"MC172851",
		"MC167983",
	],
)

result = await graph_client.admin.service_announcement.messages.unarchive.post(request_body)


```