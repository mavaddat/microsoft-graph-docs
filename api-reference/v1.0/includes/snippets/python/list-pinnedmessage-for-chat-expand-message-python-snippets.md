---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.chats.item.pinned_messages.pinned_messages_request_builder import PinnedMessagesRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = PinnedMessagesRequestBuilder.PinnedMessagesRequestBuilderGetQueryParameters(
		expand = ["message"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.chats.by_chat_id('chat-id').pinned_messages.get(request_configuration = request_configuration)


```