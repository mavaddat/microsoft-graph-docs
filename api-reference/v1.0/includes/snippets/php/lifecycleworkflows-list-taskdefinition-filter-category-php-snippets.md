---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\IdentityGovernance\LifecycleWorkflows\TaskDefinitions\TaskDefinitionsRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new TaskDefinitionsRequestBuilderGetRequestConfiguration();
$queryParameters = TaskDefinitionsRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = "category has 'joiner'";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->identityGovernance()->lifecycleWorkflows()->taskDefinitions()->get($requestConfiguration)->wait();

```