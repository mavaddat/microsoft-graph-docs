---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.communications.calls.by_call_id('call-id').audio_routing_groups.by_audio_routing_group_id('audioRoutingGroup-id').get()


```