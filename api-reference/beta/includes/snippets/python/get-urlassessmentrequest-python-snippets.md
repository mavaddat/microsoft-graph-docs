---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.information_protection.threat_assessment_requests.by_threat_assessment_request_id('threatAssessmentRequest-id').get()


```