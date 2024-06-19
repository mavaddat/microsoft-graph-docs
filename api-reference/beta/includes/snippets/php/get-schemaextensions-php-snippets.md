---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\SchemaExtensions\SchemaExtensionsRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new SchemaExtensionsRequestBuilderGetRequestConfiguration();
$queryParameters = SchemaExtensionsRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = "id eq 'graphlearn_test'";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->schemaExtensions()->get($requestConfiguration)->wait();

```