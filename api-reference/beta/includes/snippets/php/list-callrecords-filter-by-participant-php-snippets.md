---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Communications\CallRecords\CallRecordsRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new CallRecordsRequestBuilderGetRequestConfiguration();
$queryParameters = CallRecordsRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = "participants_v2/any(p:p/id eq '821809f5-0000-0000-0000-3b5136c0e777')";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->communications()->callRecords()->get($requestConfiguration)->wait();

```