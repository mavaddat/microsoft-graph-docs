---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.policies.token_lifetime_policies.by_token_lifetime_policy_id('tokenLifetimePolicy-id').get()


```