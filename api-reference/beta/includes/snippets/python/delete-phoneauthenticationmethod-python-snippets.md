---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.me.authentication.phone_methods.by_phone_authentication_method_id('phoneAuthenticationMethod-id').delete()


```