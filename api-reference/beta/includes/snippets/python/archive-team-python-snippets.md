---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.teams.item.archive.archive_post_request_body import ArchivePostRequestBody

graph_client = GraphServiceClient(credentials, scopes)

request_body = ArchivePostRequestBody(
)

await graph_client.teams.by_team_id('team-id').archive.post(request_body)


```