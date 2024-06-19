---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.drives.item.items.item.workbook.functions.vlookup.vlookup_request_builder import VlookupRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration
from msgraph.generated.drives.item.items.item.workbook.functions.vlookup.vlookup_post_request_body import VlookupPostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = VlookupPostRequestBody(
	lookup_value = "pear",
	table_array = TableArray(
		additional_data = {
				"address" : "Sheet1!B2:C7",
		}
	),
	col_index_num = 2,
	range_lookup = False,
)

request_configuration = RequestConfiguration()
request_configuration.headers.add("workbook-session-id", "{session-id}")


result = await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').workbook.functions.vlookup.post(request_body, request_configuration = request_configuration)


```