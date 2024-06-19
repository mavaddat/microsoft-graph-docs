---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.drives.item.items.item.invite.invite_post_request_body import InvitePostRequestBody
from msgraph_beta.generated.models.drive_recipient import DriveRecipient

graph_client = GraphServiceClient(credentials, scopes)

request_body = InvitePostRequestBody(
	recipients = [
		DriveRecipient(
			email = "robin@contoso.org",
		),
	],
	message = "Here's the file that we're collaborating on.",
	require_sign_in = True,
	send_invitation = True,
	roles = [
		"write",
	],
	password = "password123",
	expiration_date_time = "2018-07-15T14:00:00.000Z",
)

result = await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').invite.post(request_body)


```