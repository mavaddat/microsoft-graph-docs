---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\AccessPackageResourceRequest;
use Microsoft\Graph\Beta\Generated\Models\AccessPackageResource;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AccessPackageResourceRequest();
$requestBody->setCatalogId('beedadfe-01d5-4025-910b-84abb9369997');
$requestBody->setRequestType('AdminAdd');
$accessPackageResource = new AccessPackageResource();
$accessPackageResource->setOriginId('c6294667-7348-4f5a-be73-9d2c65f574f3');
$accessPackageResource->setOriginSystem('AadGroup');
$requestBody->setAccessPackageResource($accessPackageResource);

$result = $graphServiceClient->identityGovernance()->entitlementManagement()->accessPackageResourceRequests()->post($requestBody)->wait();

```