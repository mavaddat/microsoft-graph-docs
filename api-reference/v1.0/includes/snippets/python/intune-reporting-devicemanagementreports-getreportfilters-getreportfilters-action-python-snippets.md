---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.devicemanagement.reports.get_report_filters.get_report_filters_post_request_body import GetReportFiltersPostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = GetReportFiltersPostRequestBody(
	name = "Name value",
	select = [
		"Select value",
	],
	search = "Search value",
	group_by = [
		"Group By value",
	],
	order_by = [
		"Order By value",
	],
	skip = 4,
	top = 3,
	session_id = "Session Id value",
	filter = "Filter value",
)

await graph_client.device_management.reports.get_report_filters.post(request_body)


```