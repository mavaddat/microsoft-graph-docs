---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\IdentityGovernance\RoleManagementAlerts\Alerts\Item\AlertIncidents\AlertIncidentsRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new AlertIncidentsRequestBuilderGetRequestConfiguration();
$queryParameters = AlertIncidentsRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->top = 5;
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->identityGovernance()->roleManagementAlerts()->alerts()->byUnifiedRoleManagementAlertId('unifiedRoleManagementAlert-id')->alertIncidents()->get($requestConfiguration)->wait();

```