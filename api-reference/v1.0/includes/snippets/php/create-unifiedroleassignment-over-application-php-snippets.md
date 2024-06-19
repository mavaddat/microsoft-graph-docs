---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\UnifiedRoleAssignment;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new UnifiedRoleAssignment();
$requestBody->setOdataType('#microsoft.graph.unifiedRoleAssignment');
$requestBody->setPrincipalId('6b937a9d-c731-465b-a844-2d5b5368c161');
$requestBody->setRoleDefinitionId('9b895d92-2cd3-44c7-9d02-a6ac2d5ea5c3');
$requestBody->setDirectoryScopeId('/661e1310-bd76-4795-89a7-8f3c8f855bfc');

$result = $graphServiceClient->roleManagement()->directory()->roleAssignments()->post($requestBody)->wait();

```