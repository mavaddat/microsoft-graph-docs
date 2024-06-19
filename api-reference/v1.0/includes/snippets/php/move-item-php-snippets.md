---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\DriveItem;
use Microsoft\Graph\Generated\Models\ItemReference;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new DriveItem();
$parentReference = new ItemReference();
$parentReference->setId('{new-parent-folder-id}');
$requestBody->setParentReference($parentReference);
$requestBody->setName('new-item-name.txt');

$result = $graphServiceClient->drives()->byDriveId('drive-id')->items()->byDriveItemId('driveItem-id')->patch($requestBody)->wait();

```