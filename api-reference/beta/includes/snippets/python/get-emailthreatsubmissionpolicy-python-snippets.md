---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.security.threat_submission.email_threat_submission_policies.by_email_threat_submission_policy_id('emailThreatSubmissionPolicy-id').get()


```