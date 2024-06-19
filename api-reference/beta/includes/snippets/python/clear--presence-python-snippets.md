---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.users.item.presence.clear_presence.clear_presence_post_request_body import ClearPresencePostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = ClearPresencePostRequestBody(
	session_id = "22553876-f5ab-4529-bffb-cfe50aa89f87",
)

await graph_client.users.by_user_id('user-id').presence.clear_presence.post(request_body)


```