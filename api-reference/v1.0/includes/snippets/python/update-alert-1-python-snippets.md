---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.models.alert import Alert
from msgraph.generated.models.alert_feedback import AlertFeedback
from msgraph.generated.models.alert_status import AlertStatus
from msgraph.generated.models.security_vendor_information import SecurityVendorInformation

graph_client = GraphServiceClient(credentials, scopes)

request_body = Alert(
	assigned_to = "String",
	closed_date_time = "String (timestamp)",
	comments = [
		"String",
	],
	feedback = AlertFeedback.Unknown,
	status = AlertStatus.Unknown,
	tags = [
		"String",
	],
	vendor_information = SecurityVendorInformation(
		provider = "String",
		vendor = "String",
	),
)

result = await graph_client.security.alerts.by_alert_id('alert-id').patch(request_body)


```