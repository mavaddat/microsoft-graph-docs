---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.users.by_user_id('user-id').authentication.windows_hello_for_business_methods.by_windows_hello_for_business_authentication_method_id('windowsHelloForBusinessAuthenticationMethod-id').get()


```