---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient

graph_client = GraphServiceClient(credentials, scopes)


await graph_client.solutions.booking_businesses.by_booking_business_id('bookingBusiness-id').services.by_booking_service_id('bookingService-id').delete()


```