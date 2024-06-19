---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.security.subcategory_template import SubcategoryTemplate

graph_client = GraphServiceClient(credentials, scopes)

request_body = SubcategoryTemplate(
	odata_type = "#microsoft.graph.security.subcategoryTemplate",
	display_name = "Vendor Invoice",
)

result = await graph_client.security.labels.categories.by_category_template_id('categoryTemplate-id').subcategories.post(request_body)


```