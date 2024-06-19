---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.security.attack_simulation.trainings.item.language_details.item.training_language_detail_item_request_builder import TrainingLanguageDetailItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = TrainingLanguageDetailItemRequestBuilder.TrainingLanguageDetailItemRequestBuilderGetQueryParameters(
		filter = "locale eq 'en'",
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.security.attack_simulation.trainings.by_training_id('training-id').language_details.by_training_language_detail_id('trainingLanguageDetail-id').get(request_configuration = request_configuration)


```