---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Communications\Calls\Item\Participants\Item\StopHoldMusic\StopHoldMusicPostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new StopHoldMusicPostRequestBody();
$requestBody->setClientContext('d45324c1-fcb5-430a-902c-f20af696537c');

$result = $graphServiceClient->communications()->calls()->byCallId('call-id')->participants()->byParticipantId('participant-id')->stopHoldMusic()->post($requestBody)->wait();

```