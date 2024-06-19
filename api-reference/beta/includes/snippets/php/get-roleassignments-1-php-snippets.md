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
$queryParameters->filter = "roleDefinitionId eq '62e90394-69f5-4237-9190-012177145e10'";
$queryParameters->expand = ["principal"];
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->roleManagement()->directory()->roleAssignments()->get($requestConfiguration)->wait();

```