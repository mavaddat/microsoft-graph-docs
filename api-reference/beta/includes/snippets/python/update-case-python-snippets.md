---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.ediscovery.case import Case

graph_client = GraphServiceClient(credentials, scopes)

request_body = Case(
	display_name = "My Case 1 - Renamed",
	description = "Updated description",
	external_id = "Updated externalId",
)

result = await graph_client.compliance.ediscovery.cases.by_case_id('case-id').patch(request_body)


```