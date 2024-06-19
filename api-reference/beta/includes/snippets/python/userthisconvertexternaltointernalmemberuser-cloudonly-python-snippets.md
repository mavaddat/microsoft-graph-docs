---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.users.item.convert_external_to_internal_member_user.convert_external_to_internal_member_user_post_request_body import ConvertExternalToInternalMemberUserPostRequestBody
from msgraph_beta.generated.models.password_profile import PasswordProfile

graph_client = GraphServiceClient(credentials, scopes)

request_body = ConvertExternalToInternalMemberUserPostRequestBody(
	user_principal_name = "AdeleVance@contoso.com",
	password_profile = PasswordProfile(
		password = "Zdi087#2jhkahf",
		force_change_password_next_sign_in = True,
	),
)

result = await graph_client.users.by_user_id('user-id').convert_external_to_internal_member_user.post(request_body)


```