---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.education_category import EducationCategory

graph_client = GraphServiceClient(credentials, scopes)

request_body = EducationCategory(
	display_name = "Quizzes",
)

result = await graph_client.education.classes.by_education_class_id('educationClass-id').assignment_categories.post(request_body)


```