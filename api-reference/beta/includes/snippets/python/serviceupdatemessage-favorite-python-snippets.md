---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.admin.serviceannouncement.messages.favorite.favorite_post_request_body import FavoritePostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = FavoritePostRequestBody(
	message_ids = [
		"MC172851",
		"MC167983",
	],
)

result = await graph_client.admin.service_announcement.messages.favorite.post(request_body)


```