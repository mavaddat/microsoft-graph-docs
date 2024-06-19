---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.user_insights_settings import UserInsightsSettings

graph_client = GraphServiceClient(credentials, scopes)

request_body = UserInsightsSettings(
	is_enabled = False,
)

result = await graph_client.users.by_user_id('user-id').settings.item_insights.patch(request_body)


```