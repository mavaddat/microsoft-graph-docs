---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Reports\AppCredentialSignInActivities\AppCredentialSignInActivitiesRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new AppCredentialSignInActivitiesRequestBuilderGetRequestConfiguration();
$queryParameters = AppCredentialSignInActivitiesRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = "keyId eq '83f45296-fb8f-4aaa-a399-ac51084e02b7'";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->reports()->appCredentialSignInActivities()->get($requestConfiguration)->wait();

```