---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\DriveItem;
use Microsoft\Graph\Beta\Generated\Models\Bundle;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new DriveItem();
$requestBody->setName('Just some files');
$bundle = new Bundle();
$requestBody->setBundle($bundle);
$childrenDriveItem1 = new DriveItem();
$childrenDriveItem1->setId('1234asdf');
$childrenArray []= $childrenDriveItem1;
$childrenDriveItem2 = new DriveItem();
$childrenDriveItem2->setId('1234qwerty');
$childrenArray []= $childrenDriveItem2;
$requestBody->setChildren($childrenArray);

$additionalData = [
'@microsoft.graph.conflictBehavior' => 'rename',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->drives()->byDriveId('drive-id')->bundles()->post($requestBody)->wait();

```