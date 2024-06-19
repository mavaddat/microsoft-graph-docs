---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.users.item.events.item.event_item_request_builder import EventItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = EventItemRequestBuilder.EventItemRequestBuilderGetQueryParameters(
		select = ["subject","body","bodyPreview","organizer","attendees","start","end","location","locations"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.me.events.by_event_id('event-id').get(request_configuration = request_configuration)


```