---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\DeviceManagement\VirtualEndpoint\Reports\GetInaccessibleCloudPcReports\GetInaccessibleCloudPcReportsPostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new GetInaccessibleCloudPcReportsPostRequestBody();
$requestBody->setFilter('region eq \'westus2\'');
$requestBody->setOrderBy(['cloudPcId', 	]);
$requestBody->setSelect(['cloudPcId', 'aadDeviceId', 'cloudPcName', 'userPrincipalName', 'provisioningStatus', 'region', 'deviceHealthStatus', 'deviceHealthStatusDateTime', 'recentDeviceHealthFailureCount', 'recentConnectionFailureCount', 'systemStatus', 'systemStatusDateTime', 	]);
$requestBody->setTop(10);
$requestBody->setSkip(0);

$graphServiceClient->deviceManagement()->virtualEndpoint()->reports()->getInaccessibleCloudPcReports()->post($requestBody)->wait();

```