---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.drive_item import DriveItem

graph_client = GraphServiceClient(credentials, scopes)

request_body = DriveItem(
	name = "new-file-name.docx",
)

result = await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').patch(request_body)


```