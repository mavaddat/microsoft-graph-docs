---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.organization.item.branding.branding_request_builder import BrandingRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)


request_configuration = RequestConfiguration()
request_configuration.headers.add("Accept-Language", "fr-FR")


result = await graph_client.organization.by_organization_id('organization-id').branding.get(request_configuration = request_configuration)


```