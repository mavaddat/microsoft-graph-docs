---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Reports\GetM365AppUserDetail(period='{period}')\GetM365AppUserDetailWithPeriodRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new GetM365AppUserDetailWithPeriodRequestBuilderGetRequestConfiguration();
$queryParameters = GetM365AppUserDetailWithPeriodRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->format = "application/json";
$requestConfiguration->queryParameters = $queryParameters;


$graphServiceClient->reports()->getM365AppUserDetailWithPeriod('{period}', )->get($requestConfiguration)->wait();

```