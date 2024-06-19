---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Users\Item\Presence\SetUserPreferredPresence\SetUserPreferredPresencePostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SetUserPreferredPresencePostRequestBody();
$requestBody->setAvailability('DoNotDisturb');
$requestBody->setActivity('DoNotDisturb');
$requestBody->setExpirationDuration(new \DateInterval('PT8H'));

$graphServiceClient->users()->byUserId('user-id')->presence()->setUserPreferredPresence()->post($requestBody)->wait();

```