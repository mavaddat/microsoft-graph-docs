---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.access_reviews.access_reviews_request_builder import AccessReviewsRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = AccessReviewsRequestBuilder.AccessReviewsRequestBuilderGetQueryParameters(
		filter = "businessFlowTemplateId eq '6e4f3d20-c5c3-407f-9695-8460952bcc68'",
		top = 100,
		skip = 0,
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.access_reviews.get(request_configuration = request_configuration)


```