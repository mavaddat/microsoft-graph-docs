---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.education.classes.by_education_class_id('educationClass-id').modules.by_education_module_id('educationModule-id').delete()


```