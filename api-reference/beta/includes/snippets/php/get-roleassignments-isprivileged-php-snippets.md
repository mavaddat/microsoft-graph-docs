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
$queryParameters->expand = ["roleDefinition"];
$queryParameters->filter = "roleDefinition/isPrivileged eq true";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->roleManagement()->directory()->roleAssignments()->get($requestConfiguration)->wait();

```