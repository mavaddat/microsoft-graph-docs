---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\RoleManagement\Directory\RoleAssignments\RoleAssignmentsRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new RoleAssignmentsRequestBuilderGetRequestConfiguration();
$queryParameters = RoleAssignmentsRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = " principalId eq 'f1847572-48aa-47aa-96a3-2ec61904f41f'";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->roleManagement()->directory()->roleAssignments()->get($requestConfiguration)->wait();

```