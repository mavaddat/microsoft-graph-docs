---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.security.attack_simulation.simulation_automations.by_simulation_automation_id('simulationAutomation-id').runs.get()


```