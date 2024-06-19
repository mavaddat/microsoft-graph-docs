---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.devicemanagement.exchangeconnectors.item.sync.sync_post_request_body import SyncPostRequestBody
from msgraph.generated.models.device_management_exchange_connector_sync_type import DeviceManagementExchangeConnectorSyncType

graph_client = GraphServiceClient(credentials, scopes)

request_body = SyncPostRequestBody(
	sync_type = DeviceManagementExchangeConnectorSyncType.DeltaSync,
)

await graph_client.device_management.exchange_connectors.by_device_management_exchange_connector_id('deviceManagementExchangeConnector-id').sync.post(request_body)


```