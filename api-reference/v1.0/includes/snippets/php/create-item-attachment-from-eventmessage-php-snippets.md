---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Attachment;
use Microsoft\Graph\Generated\Models\Message;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Attachment();
$requestBody->setOdataType('#Microsoft.OutlookServices.ItemAttachment');
$requestBody->setName('name-value');
$additionalData = [
	'item' => [
		'@odata.type' => 'microsoft.graph.message',
	],
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->me()->events()->byEventId('event-id')->attachments()->post($requestBody)->wait();

```