---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.web_account import WebAccount
from msgraph_beta.generated.models.service_information import ServiceInformation

graph_client = GraphServiceClient(credentials, scopes)

request_body = WebAccount(
	description = "My Github contributions!",
	user_id = "innocenty.popov",
	service = ServiceInformation(
		name = "GitHub",
		web_url = "https://github.com",
	),
)

result = await graph_client.me.profile.web_accounts.post(request_body)


```