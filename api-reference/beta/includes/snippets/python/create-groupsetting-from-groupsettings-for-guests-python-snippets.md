---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.directory_setting import DirectorySetting
from msgraph_beta.generated.models.setting_value import SettingValue

graph_client = GraphServiceClient(credentials, scopes)

request_body = DirectorySetting(
	template_id = "08d542b9-071f-4e16-94b0-74abb372e3d9",
	values = [
		SettingValue(
			name = "AllowToAddGuests",
			value = "false",
		),
	],
)

result = await graph_client.groups.by_group_id('group-id').settings.post(request_body)


```