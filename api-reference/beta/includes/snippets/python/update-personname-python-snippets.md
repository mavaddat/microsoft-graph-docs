---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.person_name import PersonName

graph_client = GraphServiceClient(credentials, scopes)

request_body = PersonName(
	nickname = "Kesha",
)

result = await graph_client.me.profile.names.by_person_name_id('personName-id').patch(request_body)


```