---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.team import Team
from msgraph_beta.generated.models.conversation_member import ConversationMember
from msgraph_beta.generated.models.aad_user_conversation_member import AadUserConversationMember

graph_client = GraphServiceClient(credentials, scopes)

request_body = Team(
	display_name = "My Sample Team",
	description = "My Sample Team’s Description",
	members = [
		AadUserConversationMember(
			odata_type = "#microsoft.graph.aadUserConversationMember",
			roles = [
				"owner",
			],
			additional_data = {
					"user@odata_bind" : "https://graph.microsoft.com/beta/users('0040b377-61d8-43db-94f5-81374122dc7e')",
			}
		),
	],
	additional_data = {
			"template@odata_bind" : "https://graph.microsoft.com/beta/teamsTemplates('standard')",
	}
)

result = await graph_client.teams.post(request_body)


```