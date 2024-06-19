---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.exchange_restore_session import ExchangeRestoreSession

graph_client = GraphServiceClient(credentials, scopes)

request_body = ExchangeRestoreSession(
	additional_data = {
			"mailbox_restore_artifacts@delta" : [
				{
						"restore_point" : {
								"@odata_id" : "1b014d8c-71fe-4d00-a01a-31850bc5b32c",
						},
						"destination_type" : "inPlace",
				},
				{
						"restore_point" : {
								"@odata_id" : "2b014d8c-71fe-4d00-a01a-31850bc5b32",
						},
						"destination_type" : "inPlace",
				},
				{
						"restore_point" : {
								"@odata_id" : "3b014d8c-71fe-4d00-a01a-31850bc5b32c",
						},
						"destination_type" : "inPlace",
				},
				{
						"restore_point" : {
								"@odata_id" : "4b014d8c-71fe-4d00-a01a-31850bc5b32c",
						},
						"destination_type" : "inPlace",
				},
				{
						"@removed" : {
								"reason" : "changed",
						},
						"id" : "99954f18-c8ec-4b62-85bf-cdf3b70b140e",
				},
				{
						"@removed" : {
								"reason" : "changed",
						},
						"id" : "4267e382-71a9-4c07-bef7-bda97e09c0d2",
				},
				{
						"@removed" : {
								"reason" : "changed",
						},
						"id" : "3667e382-71a9-4c07-bef7-bda97e09c0d2",
				},
			],
	}
)

result = await graph_client.solutions.backup_restore.exchange_restore_sessions.by_exchange_restore_session_id('exchangeRestoreSession-id').patch(request_body)


```