---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.role_management.directory.role_definitions.by_unified_role_definition_id('unifiedRoleDefinition-id').get()


```