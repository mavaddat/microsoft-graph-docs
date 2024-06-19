---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Teams\Item\Schedule\Share\SharePostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SharePostRequestBody();
$requestBody->setNotifyTeam(true);
$requestBody->setStartDateTime(new \DateTime('2018-10-08T00:00:00.000Z'));
$requestBody->setEndDateTime(new \DateTime('2018-10-15T00:00:00.000Z'));

$graphServiceClient->teams()->byTeamId('team-id')->schedule()->share()->post($requestBody)->wait();

```