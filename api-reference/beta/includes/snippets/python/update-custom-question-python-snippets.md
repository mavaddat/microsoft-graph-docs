---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.meeting_registration_question import MeetingRegistrationQuestion
from msgraph_beta.generated.models.answer_input_type import AnswerInputType

graph_client = GraphServiceClient(credentials, scopes)

request_body = MeetingRegistrationQuestion(
	answer_input_type = AnswerInputType.RadioButton,
	answer_options = [
		"Software Engineer",
		"Software Development Manager",
		"Product Manager",
		"Data scientist",
		"Other",
	],
)

result = await graph_client.me.online_meetings.by_online_meeting_id('onlineMeeting-id').registration.custom_questions.by_meeting_registration_question_id('meetingRegistrationQuestion-id').patch(request_body)


```