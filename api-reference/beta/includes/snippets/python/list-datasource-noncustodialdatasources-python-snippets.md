---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.compliance.ediscovery.cases.by_case_id('case-id').noncustodial_data_sources.by_noncustodial_data_source_id('noncustodialDataSource-id').data_source.get()


```