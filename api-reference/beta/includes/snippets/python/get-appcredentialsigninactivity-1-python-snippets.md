---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.reports.app_credential_sign_in_activities.by_app_credential_sign_in_activity_id('appCredentialSignInActivity-id').get()


```