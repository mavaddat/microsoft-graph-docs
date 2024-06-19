---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.chat import Chat
from msgraph_beta.generated.models.chat_type import ChatType
from msgraph_beta.generated.models.conversation_member import ConversationMember
from msgraph_beta.generated.models.aad_user_conversation_member import AadUserConversationMember

graph_client = GraphServiceClient(credentials, scopes)

request_body = Chat(
	chat_type = ChatType.OneOnOne,
	members = [
		AadUserConversationMember(
			odata_type = "#microsoft.graph.aadUserConversationMember",
			roles = [
				"owner",
			],
			additional_data = {
					"user@odata_bind" : "https://graph.microsoft.com/beta/users('jacob@contoso.com')",
			}
		),
		AadUserConversationMember(
			odata_type = "#microsoft.graph.aadUserConversationMember",
			roles = [
				"owner",
			],
			additional_data = {
					"user@odata_bind" : "https://graph.microsoft.com/beta/users('alex@contoso.com')",
			}
		),
	],
)

result = await graph_client.chats.post(request_body)


```