---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.print.printers.by_printer_id('printer-id').task_triggers.by_print_task_trigger_id('printTaskTrigger-id').get()


```