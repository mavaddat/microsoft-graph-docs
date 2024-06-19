---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.identity_governance.entitlement_management.assignments.additional_access(access_package_id='{access_package_id}',incompatible_access_package_id='{incompatible_access_package_id}').additional_access_with_access_package_id_with_incompatible_access_package_id_request_builder import AdditionalAccessWithAccessPackageIdWithIncompatibleAccessPackageIdRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = AdditionalAccessWithAccessPackageIdWithIncompatibleAccessPackageIdRequestBuilder.AdditionalAccessWithAccessPackageIdWithIncompatibleAccessPackageIdRequestBuilderGetQueryParameters(
		expand = ["target"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity_governance.entitlement_management.assignments.additional_access_with_access_package_id_with_incompatible_access_package_id("{accessPackageId}","{incompatibleAccessPackageId}").get(request_configuration = request_configuration)


```