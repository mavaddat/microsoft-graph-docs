---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.identity_governance.entitlement_management.access_package_assignment_requests.filter_by_current_user_with_on("target").get()


```