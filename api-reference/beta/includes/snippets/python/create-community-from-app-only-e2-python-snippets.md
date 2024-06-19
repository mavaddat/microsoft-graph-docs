---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.community import Community
from msgraph_beta.generated.models.community_privacy import CommunityPrivacy

graph_client = GraphServiceClient(credentials, scopes)

request_body = Community(
	display_name = "Financial Advice for Software Engineers",
	description = "A community where financial advisors who represent customers from software engineering profession can discuss advice and suggestions for their clients.",
	privacy = CommunityPrivacy.Public,
	additional_data = {
			"owners@odata_bind" : [
				"https://graph.microsoft.com/beta/users/26be1845-4119-4801-a799-aea79d09f1a2",
			],
	}
)

result = await graph_client.employee_experience.communities.post(request_body)


```