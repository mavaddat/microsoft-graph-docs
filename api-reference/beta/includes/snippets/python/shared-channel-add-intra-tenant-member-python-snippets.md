---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.aad_user_conversation_member import AadUserConversationMember

graph_client = GraphServiceClient(credentials, scopes)

request_body = AadUserConversationMember(
	odata_type = "#microsoft.graph.aadUserConversationMember",
	roles = [
	],
	additional_data = {
			"user@odata_bind" : "https://graph.microsoft.com/beta/users/24b3819b-4e1d-4f3e-86bd-e42b54d0b2b4",
	}
)

result = await graph_client.teams.by_team_id('team-id').channels.by_channel_id('channel-id').members.post(request_body)


```