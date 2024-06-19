---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Teams\Item\Schedule\OfferShiftRequests\OfferShiftRequestsRequestBuilderPostRequestConfiguration;
use Microsoft\Graph\Beta\Generated\Models\OfferShiftRequest;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new OfferShiftRequest();
$requestBody->setSenderShiftId('SHFT_f7e484ed-fdd6-421c-92d9-0bc9e62e2c29');
$requestBody->setSenderMessage('Having a family emergency, could you take this shift for me?');
$requestBody->setRecipientUserId('fe278b61-21ac-4872-8b41-1962bbb98e3c');
$requestConfiguration = new OfferShiftRequestsRequestBuilderPostRequestConfiguration();
$headers = [
		'Authorization' => 'Bearer {token}',
	];
$requestConfiguration->headers = $headers;


$result = $graphServiceClient->teams()->byTeamId('team-id')->schedule()->offerShiftRequests()->post($requestBody, $requestConfiguration)->wait();

```