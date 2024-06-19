---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\IdentityProtection\RiskDetections\RiskDetectionsRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new RiskDetectionsRequestBuilderGetRequestConfiguration();
$queryParameters = RiskDetectionsRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = "userDisplayName eq 'MyTestUser1'";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->identityProtection()->riskDetections()->get($requestConfiguration)->wait();

```