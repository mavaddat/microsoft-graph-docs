---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.term_store.groups.by_group_id('group-id').sets.by_set_id('set-id').terms.by_term_id('term-id').get()


```