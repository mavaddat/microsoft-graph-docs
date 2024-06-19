---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.reports.partners.billing.usage.unbilled.microsoft_graph_partners_billing_export.export_post_request_body import ExportPostRequestBody
from msgraph.generated.models.attribute_set import AttributeSet
from msgraph.generated.models.billing_period import BillingPeriod

graph_client = GraphServiceClient(credentials, scopes)

request_body = ExportPostRequestBody(
	currency_code = "USD",
	attribute_set = AttributeSet.Full,
	billing_period = BillingPeriod.Current,
)

result = await graph_client.reports.partners.billing.usage.unbilled.microsoft_graph_partners_billing_export.post(request_body)


```