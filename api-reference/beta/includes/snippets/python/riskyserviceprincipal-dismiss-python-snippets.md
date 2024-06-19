---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.identityprotection.riskyserviceprincipals.dismiss.dismiss_post_request_body import DismissPostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = DismissPostRequestBody(
	service_principal_ids = [
		"9089a539-a539-9089-39a5-899039a58990",
	],
)

await graph_client.identity_protection.risky_service_principals.dismiss.post(request_body)


```