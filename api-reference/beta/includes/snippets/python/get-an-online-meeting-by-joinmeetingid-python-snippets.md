---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.users.item.online_meetings.online_meetings_request_builder import OnlineMeetingsRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = OnlineMeetingsRequestBuilder.OnlineMeetingsRequestBuilderGetQueryParameters(
		filter = "joinMeetingIdSettings/joinMeetingId eq '1234567890'",
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.me.online_meetings.get(request_configuration = request_configuration)


```