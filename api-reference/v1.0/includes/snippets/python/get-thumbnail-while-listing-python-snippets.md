---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.drives.item.items.item.children.children_request_builder import ChildrenRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = ChildrenRequestBuilder.ChildrenRequestBuilderGetQueryParameters(
		expand = ["thumbnails"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').children.get(request_configuration = request_configuration)


```