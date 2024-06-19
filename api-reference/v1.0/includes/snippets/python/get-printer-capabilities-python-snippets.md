---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.print.printers.item.printer_item_request_builder import PrinterItemRequestBuilder
from kiota_abstractions.base_request_configuration import RequestConfiguration

graph_client = GraphServiceClient(credentials, scopes)

query_params = PrinterItemRequestBuilder.PrinterItemRequestBuilderGetQueryParameters(
		select = ["id","displayName","capabilities"],
)

request_configuration = RequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.print.printers.by_printer_id('printer-id').get(request_configuration = request_configuration)


```