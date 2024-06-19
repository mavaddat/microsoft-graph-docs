---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Directory\Recommendations\Item\Postpone\PostponePostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new PostponePostRequestBody();
$requestBody->setPostponeUntilDateTime(new \DateTime('2023-02-01T02:53:00Z'));

$result = $graphServiceClient->directory()->recommendations()->byRecommendationId('recommendation-id')->postpone()->post($requestBody)->wait();

```