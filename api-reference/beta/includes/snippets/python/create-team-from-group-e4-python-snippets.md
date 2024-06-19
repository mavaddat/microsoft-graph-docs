---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.team import Team

graph_client = GraphServiceClient(credentials, scopes)

request_body = Team(
	additional_data = {
			"template@odata_bind" : "https://graph.microsoft.com/beta/teamsTemplates('standard')",
			"group@odata_bind" : "https://graph.microsoft.com/beta/groups('71392b2f-1765-406e-86af-5907d9bdb2ab')",
	}
)

result = await graph_client.teams.post(request_body)


```