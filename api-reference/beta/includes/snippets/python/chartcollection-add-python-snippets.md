---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.drives.item.items.item.workbook.worksheets.item.charts.add.add_post_request_body import AddPostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = AddPostRequestBody(
	type = "ColumnStacked",
	source_data = "A1:B1",
	series_by = "Auto",
)

result = await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').workbook.worksheets.by_workbook_worksheet_id('workbookWorksheet-id').charts.add.post(request_body)


```