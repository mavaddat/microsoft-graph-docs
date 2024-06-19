---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.serviceprincipals.item.synchronization.jobs.item.validate_credentials.validate_credentials_post_request_body import ValidateCredentialsPostRequestBody
from msgraph_beta.generated.models.synchronization_secret_key_string_value_pair import SynchronizationSecretKeyStringValuePair
from msgraph_beta.generated.models.synchronization_secret import SynchronizationSecret

graph_client = GraphServiceClient(credentials, scopes)

request_body = ValidateCredentialsPostRequestBody(
	credentials = [
		SynchronizationSecretKeyStringValuePair(
			key = SynchronizationSecret.UserName,
			value = "user@domain.com",
		),
		SynchronizationSecretKeyStringValuePair(
			key = SynchronizationSecret.Password,
			value = "password-value",
		),
	],
)

await graph_client.service_principals.by_service_principal_id('servicePrincipal-id').synchronization.jobs.by_synchronization_job_id('synchronizationJob-id').validate_credentials.post(request_body)


```