---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.education.classes.by_education_class_id('educationClass-id').assignment_categories.by_education_category_id('educationCategory-id').delete()


```