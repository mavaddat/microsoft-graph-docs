---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.education_module_resource import EducationModuleResource
from msgraph_beta.generated.models.education_resource import EducationResource

graph_client = GraphServiceClient(credentials, scopes)

request_body = EducationModuleResource(
	resource = EducationResource(
		display_name = "new pdf file patched.pdf",
	),
)

result = await graph_client.education.classes.by_education_class_id('educationClass-id').modules.by_education_module_id('educationModule-id').resources.by_education_module_resource_id('educationModuleResource-id').patch(request_body)


```