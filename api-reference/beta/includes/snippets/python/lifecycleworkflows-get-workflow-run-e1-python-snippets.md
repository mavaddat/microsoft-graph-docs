---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.identity_governance.lifecycle_workflows.workflows.by_workflow_id('workflow-id').runs.by_run_id('run-id').get()


```