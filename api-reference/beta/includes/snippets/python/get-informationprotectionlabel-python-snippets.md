---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.me.information_protection.policy.labels.by_information_protection_label_id('informationProtectionLabel-id').get()


```