---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.drives.item.items.item.workbook.tables.add.add_post_request_body import AddPostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = AddPostRequestBody(
	address = "Sheet1!A1:D5",
	has_headers = True,
)

result = await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').workbook.tables.add.post(request_body)


```