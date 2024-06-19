---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Event;
use Microsoft\Graph\Beta\Generated\Models\ResponseStatus;
use Microsoft\Graph\Beta\Generated\Models\ResponseType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Event();
$requestBody->setOriginalStartTimeZone('originalStartTimeZone-value');
$requestBody->setOriginalEndTimeZone('originalEndTimeZone-value');
$responseStatus = new ResponseStatus();
$responseStatus->setResponse(new ResponseType('none'));
$responseStatus->setTime(new \DateTime('datetime-value'));
$requestBody->setResponseStatus($responseStatus);
$requestBody->setUid('iCalUId-value');
$requestBody->setReminderMinutesBeforeStart(99);
$requestBody->setIsReminderOn(true);

$result = $graphServiceClient->groups()->byGroupId('group-id')->events()->byEventId('event-id')->patch($requestBody)->wait();

```