---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.tenant_relationships.managed_tenants.device_compliance_policy_setting_state_summaries.by_device_compliance_policy_setting_state_summary_id('deviceCompliancePolicySettingStateSummary-id').get()


```