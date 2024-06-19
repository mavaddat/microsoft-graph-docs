---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\WorkplaceSensorDevice;
use Microsoft\Graph\Beta\Generated\Models\WorkplaceSensor;
use Microsoft\Graph\Beta\Generated\Models\WorkplaceSensorType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new WorkplaceSensorDevice();
$requestBody->setDeviceId('contoso_9D6816');
$requestBody->setDisplayName('Contoso 9D6816 Device');
$requestBody->setDescription('Contoso 9D6816 Device');
$requestBody->setMacAddress('00:0A:95:9D:68:16');
$requestBody->setManufacturer('Contoso');
$requestBody->setIpV4Address('192.168.1.100');
$requestBody->setIpV6Address('2001:db8::ff00:42:8329');
$requestBody->setPlaceId('acfa3bc0-2b83-425b-8910-84a0250e9671');
$requestBody->setTags(['Building A', 'Floor 3', 'Room 301', 'Conference Room', 'v1.0.7', 	]);
$sensorsWorkplaceSensor1 = new WorkplaceSensor();
$sensorsWorkplaceSensor1->setSensorType(new WorkplaceSensorType('occupancy'));
$sensorsArray []= $sensorsWorkplaceSensor1;
$sensorsWorkplaceSensor2 = new WorkplaceSensor();
$sensorsWorkplaceSensor2->setSensorType(new WorkplaceSensorType('peopleCount'));
$sensorsArray []= $sensorsWorkplaceSensor2;
$requestBody->setSensors($sensorsArray);


$result = $graphServiceClient->workplace()->sensorDevices()->byWorkplaceSensorDeviceId('workplaceSensorDevice-id')->patch($requestBody)->wait();

```