---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.identitygovernance.entitlementmanagement.accesspackageassignmentrequests.item.cancel.cancel_post_request_body import CancelPostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = CancelPostRequestBody(
	additional_data = {
			"id" : "request-id",
			"request_status" : "cancelled",
	}
)

await graph_client.identity_governance.entitlement_management.access_package_assignment_requests.by_access_package_assignment_request_id('accessPackageAssignmentRequest-id').cancel.post(request_body)


```