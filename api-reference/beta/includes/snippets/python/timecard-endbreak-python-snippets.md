---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.teams.item.schedule.timecards.item.end_break.end_break_post_request_body import EndBreakPostRequestBody
from msgraph_beta.generated.models.item_body import ItemBody
from msgraph_beta.generated.models.body_type import BodyType

graph_client = GraphServiceClient(credentials, scopes)

request_body = EndBreakPostRequestBody(
	notes = ItemBody(
		content_type = BodyType.Text,
		content = "end break smaple notes",
	),
	additional_data = {
			"at_aproved_location" : True,
	}
)

result = await graph_client.teams.by_team_id('team-id').schedule.time_cards.by_time_card_id('timeCard-id').end_break.post(request_body)


```