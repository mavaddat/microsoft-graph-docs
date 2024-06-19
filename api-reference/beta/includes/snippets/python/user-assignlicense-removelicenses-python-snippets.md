---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.users.item.assign_license.assign_license_post_request_body import AssignLicensePostRequestBody
from msgraph_beta.generated.models.assigned_license import AssignedLicense

graph_client = GraphServiceClient(credentials, scopes)

request_body = AssignLicensePostRequestBody(
	add_licenses = [
	],
	remove_licenses = [
		UUID("f30db892-07e9-47e9-837c-80727f46fd3d"),
		UUID("84a661c4-e949-4bd2-a560-ed7766fcaf2b"),
	],
)

result = await graph_client.me.assign_license.post(request_body)


```