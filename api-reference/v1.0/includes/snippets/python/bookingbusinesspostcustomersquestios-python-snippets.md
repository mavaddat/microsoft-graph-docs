---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.models.booking_custom_question import BookingCustomQuestion
from msgraph.generated.models.answer_input_type import AnswerInputType

graph_client = GraphServiceClient(credentials, scopes)

request_body = BookingCustomQuestion(
	odata_type = "#microsoft.graph.bookingCustomQuestion",
	display_name = "What is your age?",
	answer_input_type = AnswerInputType.Text,
	answer_options = [
	],
)

result = await graph_client.solutions.booking_businesses.by_booking_business_id('bookingBusiness-id').custom_questions.post(request_body)


```