---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Drives\Item\Items\Item\Content\ContentRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new ContentRequestBuilderGetRequestConfiguration();
$queryParameters = ContentRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->format = "{format}";
$requestConfiguration->queryParameters = $queryParameters;


$graphServiceClient->drives()->byDriveId('drive-id')->items()->byDriveItemId('driveItem-id')->content()->get($requestConfiguration)->wait();

```