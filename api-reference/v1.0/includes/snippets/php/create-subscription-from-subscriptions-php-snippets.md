---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Subscription;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Subscription();
$requestBody->setChangeType('created');
$requestBody->setNotificationUrl('https://webhook.azurewebsites.net/api/send/myNotifyClient');
$requestBody->setResource('me/mailFolders(\'Inbox\')/messages');
$requestBody->setExpirationDateTime(new \DateTime('2016-11-20T18:23:45.9356913Z'));
$requestBody->setClientState('secretClientValue');
$requestBody->setLatestSupportedTlsVersion('v1_2');

$result = $graphServiceClient->subscriptions()->post($requestBody)->wait();

```