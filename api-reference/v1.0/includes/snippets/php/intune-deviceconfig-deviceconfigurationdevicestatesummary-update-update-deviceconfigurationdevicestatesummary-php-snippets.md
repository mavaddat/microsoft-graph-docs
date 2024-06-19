---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\DeviceConfigurationDeviceStateSummary;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new DeviceConfigurationDeviceStateSummary();
$requestBody->setOdataType('#microsoft.graph.deviceConfigurationDeviceStateSummary');
$requestBody->setUnknownDeviceCount(2);
$requestBody->setNotApplicableDeviceCount(8);
$requestBody->setCompliantDeviceCount(4);
$requestBody->setRemediatedDeviceCount(5);
$requestBody->setNonCompliantDeviceCount(7);
$requestBody->setErrorDeviceCount(0);
$requestBody->setConflictDeviceCount(3);

$result = $graphServiceClient->deviceManagement()->deviceConfigurationDeviceStateSummaries()->patch($requestBody)->wait();

```