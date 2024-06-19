---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.devicemanagement.virtualendpoint.cloudpcs.item.change_user_account_type.change_user_account_type_post_request_body import ChangeUserAccountTypePostRequestBody
from msgraph_beta.generated.models.cloud_pc_user_account_type import CloudPcUserAccountType

graph_client = GraphServiceClient(credentials, scopes)

request_body = ChangeUserAccountTypePostRequestBody(
	user_account_type = CloudPcUserAccountType.Administrator,
)

await graph_client.device_management.virtual_endpoint.cloud_p_cs.by_cloud_p_c_id('cloudPC-id').change_user_account_type.post(request_body)


```