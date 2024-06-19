---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.chats.item.unhide_for_user.unhide_for_user_post_request_body import UnhideForUserPostRequestBody
from msgraph_beta.generated.models.teamwork_user_identity import TeamworkUserIdentity

graph_client = GraphServiceClient(credentials, scopes)

request_body = UnhideForUserPostRequestBody(
	user = TeamworkUserIdentity(
		id = "d864e79f-a516-4d0f-9fee-0eeb4d61fdc2",
		additional_data = {
				"tenant_id" : "2a690434-97d9-4eed-83a6-f5f13600199a",
		}
	),
)

await graph_client.chats.by_chat_id('chat-id').unhide_for_user.post(request_body)


```