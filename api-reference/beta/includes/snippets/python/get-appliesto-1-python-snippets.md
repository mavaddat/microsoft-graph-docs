---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.policies.claims_mapping_policies.by_claims_mapping_policy_id('claimsMappingPolicy-id').applies_to.get()


```