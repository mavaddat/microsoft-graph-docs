---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.drives.item.items.item.workbook.application.calculate.calculate_post_request_body import CalculatePostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = CalculatePostRequestBody(
	calculation_type = "calculationType-value",
)

await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').workbook.application.calculate.post(request_body)


```