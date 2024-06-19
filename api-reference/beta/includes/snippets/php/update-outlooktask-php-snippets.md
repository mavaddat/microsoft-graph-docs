---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Users\Item\Outlook\Tasks\Item\OutlookTaskItemRequestBuilderPatchRequestConfiguration;
use Microsoft\Graph\Beta\Generated\Models\OutlookTask;
use Microsoft\Graph\Beta\Generated\Models\DateTimeTimeZone;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new OutlookTask();
$dueDateTime = new DateTimeTimeZone();
$dueDateTime->setDateTime('2016-05-06T16:00:00');
$dueDateTime->setTimeZone('Eastern Standard Time');
$requestBody->setDueDateTime($dueDateTime);
$requestConfiguration = new OutlookTaskItemRequestBuilderPatchRequestConfiguration();
$headers = [
		'Prefer' => 'outlook.timezone="Eastern Standard Time"',
	];
$requestConfiguration->headers = $headers;


$result = $graphServiceClient->me()->outlook()->tasks()->byOutlookTaskId('outlookTask-id')->patch($requestBody, $requestConfiguration)->wait();

```