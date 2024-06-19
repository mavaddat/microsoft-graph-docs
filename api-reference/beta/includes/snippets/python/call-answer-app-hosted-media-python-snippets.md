---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.communications.calls.item.answer.answer_post_request_body import AnswerPostRequestBody
from msgraph_beta.generated.models.modality import Modality
from msgraph_beta.generated.models.app_hosted_media_config import AppHostedMediaConfig

graph_client = GraphServiceClient(credentials, scopes)

request_body = AnswerPostRequestBody(
	callback_uri = "https://bot.contoso.com/api/calls",
	accepted_modalities = [
		Modality.Audio,
	],
	media_config = AppHostedMediaConfig(
		odata_type = "#microsoft.graph.appHostedMediaConfig",
		blob = "<Media Session Configuration Blob>",
	),
)

await graph_client.communications.calls.by_call_id('call-id').answer.post(request_body)


```