---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.users.by_user_id('user-id').teamwork.installed_apps.by_user_scope_teams_app_installation_id('userScopeTeamsAppInstallation-id').chat.get()


```