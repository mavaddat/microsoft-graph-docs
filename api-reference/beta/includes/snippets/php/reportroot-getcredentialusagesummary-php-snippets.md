---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Reports\GetCredentialUsageSummary(period='{period}')\GetCredentialUsageSummaryWithPeriodRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new GetCredentialUsageSummaryWithPeriodRequestBuilderGetRequestConfiguration();
$queryParameters = GetCredentialUsageSummaryWithPeriodRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = "feature eq 'registration'";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->reports()->getCredentialUsageSummaryWithPeriod('{period}', )->get($requestConfiguration)->wait();

```