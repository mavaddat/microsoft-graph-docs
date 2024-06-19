---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.identity_user_flow_attribute_assignment import IdentityUserFlowAttributeAssignment
from msgraph_beta.generated.models.identity_user_flow_attribute_input_type import IdentityUserFlowAttributeInputType

graph_client = GraphServiceClient(credentials, scopes)

request_body = IdentityUserFlowAttributeAssignment(
	user_input_type = IdentityUserFlowAttributeInputType.TextBox,
)

result = await graph_client.identity.b2c_user_flows.by_b2c_identity_user_flow_id('b2cIdentityUserFlow-id').user_attribute_assignments.by_identity_user_flow_attribute_assignment_id('identityUserFlowAttributeAssignment-id').patch(request_body)


```