---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.channel import Channel
from msgraph_beta.generated.models.channel_membership_type import ChannelMembershipType
from msgraph_beta.generated.models.conversation_member import ConversationMember
from msgraph_beta.generated.models.aad_user_conversation_member import AadUserConversationMember

graph_client = GraphServiceClient(credentials, scopes)

request_body = Channel(
	odata_type = "#Microsoft.Graph.channel",
	membership_type = ChannelMembershipType.Private,
	display_name = "My First Private Channel",
	description = "This is my first private channels",
	members = [
		AadUserConversationMember(
			odata_type = "#microsoft.graph.aadUserConversationMember",
			roles = [
				"owner",
			],
			additional_data = {
					"user@odata_bind" : "https://graph.microsoft.com/beta/users('62855810-484b-4823-9e01-60667f8b12ae')",
			}
		),
	],
)

result = await graph_client.teams.by_team_id('team-id').channels.post(request_body)


```