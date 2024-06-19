---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.sites.item.lists.item.items.item.create_link.create_link_post_request_body import CreateLinkPostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = CreateLinkPostRequestBody(
	type = "embed",
)

result = await graph_client.sites.by_site_id('site-id').lists.by_list_id('list-id').items.by_list_item_id('listItem-id').create_link.post(request_body)


```