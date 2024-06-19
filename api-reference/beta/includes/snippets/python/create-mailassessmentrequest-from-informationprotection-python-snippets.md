---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.mail_assessment_request import MailAssessmentRequest
from msgraph_beta.generated.models.threat_expected_assessment import ThreatExpectedAssessment
from msgraph_beta.generated.models.threat_category import ThreatCategory

graph_client = GraphServiceClient(credentials, scopes)

request_body = MailAssessmentRequest(
	odata_type = "#microsoft.graph.mailAssessmentRequest",
	recipient_email = "tifc@contoso.com",
	expected_assessment = ThreatExpectedAssessment.Block,
	category = ThreatCategory.Spam,
	message_uri = "https://graph.microsoft.com/beta/users/c52ce8db-3e4b-4181-93c4-7d6b6bffaf60/messages/AAMkADU3MWUxOTU0LWNlOTEt=",
)

result = await graph_client.information_protection.threat_assessment_requests.post(request_body)


```