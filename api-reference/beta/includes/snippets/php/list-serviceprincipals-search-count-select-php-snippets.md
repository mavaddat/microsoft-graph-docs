---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\ServicePrincipals\ServicePrincipalsRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new ServicePrincipalsRequestBuilderGetRequestConfiguration();
$headers = [
		'ConsistencyLevel' => 'eventual',
	];
$requestConfiguration->headers = $headers;

$queryParameters = ServicePrincipalsRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->search = "\"displayName:Team\"";
$queryParameters->count = true;
$queryParameters->select = ["accountEnabled","displayName","publisherName","servicePrincipalType","signInAudience"];
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->servicePrincipals()->get($requestConfiguration)->wait();

```