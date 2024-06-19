---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\DeviceManagement\VirtualEndpoint\CloudPCs\BulkResize\BulkResizePostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new BulkResizePostRequestBody();
$requestBody->setCloudPcIds(['30d0e128-de93-41dc-89ec-33d84bb662a0', '7c82a3e3-9459-44e4-94d9-b92f93bf78dd', 	]);
$requestBody->setTargetServicePlanId('662009bc-7732-4f6f-8726-25883518b33e');

$result = $graphServiceClient->deviceManagement()->virtualEndpoint()->cloudPCs()->bulkResize()->post($requestBody)->wait();

```