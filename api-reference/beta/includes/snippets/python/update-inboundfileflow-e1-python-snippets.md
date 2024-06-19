---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.industry_data.inbound_file_flow import InboundFileFlow

graph_client = GraphServiceClient(credentials, scopes)

request_body = InboundFileFlow(
	odata_type = "#microsoft.graph.industryData.inboundFileFlow",
	display_name = "Updated flow name",
)

result = await graph_client.external.industry_data.inbound_flows.by_inbound_flow_id('inboundFlow-id').patch(request_body)


```