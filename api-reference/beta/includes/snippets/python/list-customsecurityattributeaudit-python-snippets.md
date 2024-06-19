---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.audit_logs.custom_security_attribute_audits.custom_security_attribute_audits_request_builder import CustomSecurityAttributeAuditsRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = CustomSecurityAttributeAuditsRequestBuilder.CustomSecurityAttributeAuditsRequestBuilderGetQueryParameters(
		top = 1,
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.audit_logs.custom_security_attribute_audits.get(request_configuration = request_configuration)


```