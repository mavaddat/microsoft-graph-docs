---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.directory.certificate_authorities.certificate_based_application_configurations.by_certificate_based_application_configuration_id('certificateBasedApplicationConfiguration-id').trusted_certificate_authorities.by_certificate_authority_as_entity_id('certificateAuthorityAsEntity-id').delete()


```