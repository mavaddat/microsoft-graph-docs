---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.identity_governance.entitlement_management.access_package_assignment_approvals.by_approval_id('approval-id').steps.by_approval_step_id('approvalStep-id').get()


```