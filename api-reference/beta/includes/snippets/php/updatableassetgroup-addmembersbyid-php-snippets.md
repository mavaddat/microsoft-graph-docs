---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Admin\Windows\Updates\UpdatableAssets\Item\MicrosoftGraphWindowsUpdatesAddMembersById\AddMembersByIdPostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AddMembersByIdPostRequestBody();
$requestBody->setIds(['String', 'String', 'String', 	]);
$requestBody->setMemberEntityType('#microsoft.graph.windowsUpdates.azureADDevice');

$graphServiceClient->admin()->windows()->updates()->updatableAssets()->byUpdatableAssetId('updatableAsset-id')->microsoftGraphWindowsUpdatesAddMembersById()->post($requestBody)->wait();

```