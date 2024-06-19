---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.b2c_identity_user_flow import B2cIdentityUserFlow
from msgraph_beta.generated.models.user_flow_type import UserFlowType
from msgraph_beta.generated.models.user_flow_api_connector_configuration import UserFlowApiConnectorConfiguration
from msgraph_beta.generated.models.identity_api_connector import IdentityApiConnector

graph_client = GraphServiceClient(credentials, scopes)

request_body = B2cIdentityUserFlow(
	id = "UserFlowWithAPIConnector",
	user_flow_type = UserFlowType.SignUpOrSignIn,
	user_flow_type_version = 1,
	api_connector_configuration = UserFlowApiConnectorConfiguration(
		post_federation_signup = IdentityApiConnector(
			additional_data = {
					"@odata_id" : "{apiConnectorId}",
			}
		),
		post_attribute_collection = IdentityApiConnector(
			additional_data = {
					"@odata_id" : "{apiConnectorId}",
			}
		),
	),
)

result = await graph_client.identity.b2c_user_flows.post(request_body)


```