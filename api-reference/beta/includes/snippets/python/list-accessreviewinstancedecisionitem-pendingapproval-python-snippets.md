---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.users.item.pending_access_review_instances.item.decisions.decisions_request_builder import DecisionsRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = DecisionsRequestBuilder.DecisionsRequestBuilderGetQueryParameters(
		top = 100,
		skip = 0,
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.me.pending_access_review_instances.by_access_review_instance_id('accessReviewInstance-id').decisions.get(request_configuration = request_configuration)


```