---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.external.connections.by_external_connection_id('externalConnection-id').operations.by_connection_operation_id('connectionOperation-id').get()


```