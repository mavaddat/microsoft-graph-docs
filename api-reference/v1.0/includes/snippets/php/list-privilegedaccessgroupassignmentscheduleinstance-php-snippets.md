---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\IdentityGovernance\PrivilegedAccess\Group\AssignmentScheduleInstances\AssignmentScheduleInstancesRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new AssignmentScheduleInstancesRequestBuilderGetRequestConfiguration();
$queryParameters = AssignmentScheduleInstancesRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = "groupId eq '2b5ed229-4072-478d-9504-a047ebd4b07d'";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->identityGovernance()->privilegedAccess()->group()->assignmentScheduleInstances()->get($requestConfiguration)->wait();

```