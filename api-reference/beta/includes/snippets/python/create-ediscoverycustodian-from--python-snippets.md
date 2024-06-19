---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.security.ediscovery_custodian import EdiscoveryCustodian

graph_client = GraphServiceClient(credentials, scopes)

request_body = EdiscoveryCustodian(
	email = "AdeleV@contoso.com",
)

result = await graph_client.security.cases.ediscovery_cases.by_ediscovery_case_id('ediscoveryCase-id').custodians.post(request_body)


```