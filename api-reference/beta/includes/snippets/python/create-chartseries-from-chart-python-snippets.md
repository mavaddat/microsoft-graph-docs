---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.workbook_chart_series import WorkbookChartSeries

graph_client = GraphServiceClient(credentials, scopes)

request_body = WorkbookChartSeries(
	name = "name-value",
)

result = await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').workbook.worksheets.by_workbook_worksheet_id('workbookWorksheet-id').charts.by_workbook_chart_id('workbookChart-id').series.post(request_body)


```