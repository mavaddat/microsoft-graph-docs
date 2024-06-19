---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.b2c_identity_user_flow import B2cIdentityUserFlow
from msgraph_beta.generated.models.user_flow_type import UserFlowType

graph_client = GraphServiceClient(credentials, scopes)

request_body = B2cIdentityUserFlow(
	id = "Customer",
	user_flow_type = UserFlowType.SignUpOrSignIn,
	user_flow_type_version = 3,
)

result = await graph_client.identity.b2c_user_flows.post(request_body)


```