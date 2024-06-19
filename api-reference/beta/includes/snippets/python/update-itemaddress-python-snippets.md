---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.item_address import ItemAddress
from msgraph_beta.generated.models.allowed_audiences import AllowedAudiences

graph_client = GraphServiceClient(credentials, scopes)

request_body = ItemAddress(
	allowed_audiences = AllowedAudiences.Me,
	display_name = "Secret Hideout",
)

result = await graph_client.users.by_user_id('user-id').profile.addresses.by_item_address_id('itemAddress-id').patch(request_body)


```