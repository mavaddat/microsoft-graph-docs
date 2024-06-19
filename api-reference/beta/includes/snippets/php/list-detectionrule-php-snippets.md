---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Security\Rules\DetectionRules\DetectionRulesRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new DetectionRulesRequestBuilderGetRequestConfiguration();
$queryParameters = DetectionRulesRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->top = 3;
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->security()->rules()->detectionRules()->get($requestConfiguration)->wait();

```