---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.security.retention_label import RetentionLabel
from msgraph_beta.generated.models.security.retention_duration_in_days import RetentionDurationInDays

graph_client = GraphServiceClient(credentials, scopes)

request_body = RetentionLabel(
	odata_type = "#microsoft.graph.security.retentionLabel",
	retention_duration = RetentionDurationInDays(
		odata_type = "microsoft.graph.security.retentionDurationInDays",
		days = 2555,
	),
)

result = await graph_client.security.labels.retention_labels.by_retention_label_id('retentionLabel-id').patch(request_body)


```