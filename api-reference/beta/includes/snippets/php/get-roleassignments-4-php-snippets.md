---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\RoleManagement\Exchange\RoleAssignments\RoleAssignmentsRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new RoleAssignmentsRequestBuilderGetRequestConfiguration();
$queryParameters = RoleAssignmentsRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = "principalId eq '/ServicePrincipals/5d39cc4d-ba68-4c44-92c7-5056e3a1ce39'";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->roleManagement()->exchange()->roleAssignments()->get($requestConfiguration)->wait();

```