---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.admin.serviceannouncement.messages.archive.archive_post_request_body import ArchivePostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = ArchivePostRequestBody(
	message_ids = [
		"MC172851",
		"MC167983",
	],
)

result = await graph_client.admin.service_announcement.messages.archive.post(request_body)


```