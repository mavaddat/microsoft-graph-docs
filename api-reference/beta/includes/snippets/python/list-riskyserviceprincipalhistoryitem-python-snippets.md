---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.identity_protection.risky_service_principals.by_risky_service_principal_id('riskyServicePrincipal-id').history.get()


```