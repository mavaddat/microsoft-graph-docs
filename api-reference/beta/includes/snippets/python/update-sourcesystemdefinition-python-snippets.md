---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.industry_data.source_system_definition import SourceSystemDefinition

graph_client = GraphServiceClient(credentials, scopes)

request_body = SourceSystemDefinition(
	vendor = "LMS Vendor",
)

result = await graph_client.external.industry_data.source_systems.by_source_system_definition_id('sourceSystemDefinition-id').patch(request_body)


```