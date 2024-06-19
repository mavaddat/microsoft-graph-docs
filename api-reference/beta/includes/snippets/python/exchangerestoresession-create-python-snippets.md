---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.exchange_restore_session import ExchangeRestoreSession
from msgraph_beta.generated.models.mailbox_restore_artifact import MailboxRestoreArtifact
from msgraph_beta.generated.models.restore_point import RestorePoint
from msgraph_beta.generated.models.destination_type import DestinationType

graph_client = GraphServiceClient(credentials, scopes)

request_body = ExchangeRestoreSession(
	mailbox_restore_artifacts = [
		MailboxRestoreArtifact(
			restore_point = RestorePoint(
				additional_data = {
						"@odata_id" : "1f1fccc3-a642-4f61-bf49-f37b9a888279",
				}
			),
			destination_type = DestinationType.InPlace,
		),
		MailboxRestoreArtifact(
			restore_point = RestorePoint(
				additional_data = {
						"@odata_id" : "1f1fccc3-a642-4f61-bf49-f37b9a888280",
				}
			),
			destination_type = DestinationType.InPlace,
		),
	],
)

result = await graph_client.solutions.backup_restore.exchange_restore_sessions.post(request_body)


```