---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.on_premises_publishing_profiles.by_on_premises_publishing_profile_id('onPremisesPublishingProfile-id').agents.by_on_premises_agent_id('onPremisesAgent-id').agent_groups.by_on_premises_agent_group_id('onPremisesAgentGroup-id').ref.delete()


```