---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.ediscovery.custodian import Custodian

graph_client = GraphServiceClient(credentials, scopes)

request_body = Custodian(
	apply_hold_to_sources = False,
)

result = await graph_client.compliance.ediscovery.cases.by_case_id('case-id').custodians.by_custodian_id('custodian-id').patch(request_body)


```