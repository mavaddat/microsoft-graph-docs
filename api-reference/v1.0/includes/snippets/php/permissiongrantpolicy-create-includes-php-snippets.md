---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\PermissionGrantConditionSet;
use Microsoft\Graph\Generated\Models\PermissionType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new PermissionGrantConditionSet();
$requestBody->setPermissionType(new PermissionType('delegated'));
$requestBody->setClientApplicationsFromVerifiedPublisherOnly(true);

$result = $graphServiceClient->policies()->permissionGrantPolicies()->byPermissionGrantPolicyId('permissionGrantPolicy-id')->includes()->post($requestBody)->wait();

```