---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.print.printers.by_printer_id('printer-id').jobs.by_print_job_id('printJob-id').documents.by_print_document_id('printDocument-id').content.get()


```