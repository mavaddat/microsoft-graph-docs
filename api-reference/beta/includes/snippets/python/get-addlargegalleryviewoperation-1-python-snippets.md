---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.communications.calls.by_call_id('call-id').operations.by_comms_operation_id('commsOperation-id').get()


```