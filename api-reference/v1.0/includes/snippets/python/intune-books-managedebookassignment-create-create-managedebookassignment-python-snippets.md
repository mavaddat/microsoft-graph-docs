---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.models.managed_e_book_assignment import ManagedEBookAssignment
from msgraph.generated.models.all_licensed_users_assignment_target import AllLicensedUsersAssignmentTarget
from msgraph.generated.models.install_intent import InstallIntent

graph_client = GraphServiceClient(credentials, scopes)

request_body = ManagedEBookAssignment(
	odata_type = "#microsoft.graph.managedEBookAssignment",
	target = AllLicensedUsersAssignmentTarget(
		odata_type = "microsoft.graph.allLicensedUsersAssignmentTarget",
	),
	install_intent = InstallIntent.Required,
)

result = await graph_client.device_app_management.managed_e_books.by_managed_e_book_id('managedEBook-id').assignments.post(request_body)


```