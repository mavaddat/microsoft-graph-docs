---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.drives.item.items.item.thumbnails.thumbnails_request_builder import ThumbnailsRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = ThumbnailsRequestBuilder.ThumbnailsRequestBuilderGetQueryParameters(
		select = ["c300x400_crop"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').thumbnails.get(request_configuration = request_configuration)


```