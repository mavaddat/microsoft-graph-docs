---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.security.ediscovery_review_tag import EdiscoveryReviewTag
from msgraph_beta.generated.models.child_selectability import ChildSelectability

graph_client = GraphServiceClient(credentials, scopes)

request_body = EdiscoveryReviewTag(
	display_name = "My tag API",
	description = "Use Graph API to create tags",
	child_selectability = ChildSelectability.Many,
)

result = await graph_client.security.cases.ediscovery_cases.by_ediscovery_case_id('ediscoveryCase-id').tags.post(request_body)


```