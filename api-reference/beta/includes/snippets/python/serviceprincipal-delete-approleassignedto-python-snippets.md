---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.service_principals.by_service_principal_id('servicePrincipal-id').app_role_assigned_to.by_app_role_assignment_id('appRoleAssignment-id').delete()


```