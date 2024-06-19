---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Groups\Item\RejectedSenders\Ref\RefRequestBuilderDeleteRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new RefRequestBuilderDeleteRequestConfiguration();
$queryParameters = RefRequestBuilderDeleteRequestConfiguration::createQueryParameters();
$queryParameters->id = "https://graph.microsoft.com/beta/users/{id}";
$requestConfiguration->queryParameters = $queryParameters;


$graphServiceClient->groups()->byGroupId('group-id')->rejectedSenders()->ref()->delete($requestConfiguration)->wait();

```