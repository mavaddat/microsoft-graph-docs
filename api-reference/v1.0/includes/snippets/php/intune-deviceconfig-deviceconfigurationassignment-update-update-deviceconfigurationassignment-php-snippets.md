---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\DeviceConfigurationAssignment;
use Microsoft\Graph\Generated\Models\ConfigurationManagerCollectionAssignmentTarget;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new DeviceConfigurationAssignment();
$requestBody->setOdataType('#microsoft.graph.deviceConfigurationAssignment');
$target = new ConfigurationManagerCollectionAssignmentTarget();
$target->setOdataType('microsoft.graph.configurationManagerCollectionAssignmentTarget');
$target->setCollectionId('Collection Id value');
$requestBody->setTarget($target);

$result = $graphServiceClient->deviceManagement()->deviceConfigurations()->byDeviceConfigurationId('deviceConfiguration-id')->assignments()->byDeviceConfigurationAssignmentId('deviceConfigurationAssignment-id')->patch($requestBody)->wait();

```