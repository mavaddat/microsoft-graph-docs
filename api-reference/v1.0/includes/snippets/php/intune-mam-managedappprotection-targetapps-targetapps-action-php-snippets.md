---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\DeviceAppManagement\ManagedAppPolicies\Item\TargetApps\TargetAppsPostRequestBody;
use Microsoft\Graph\Generated\Models\ManagedMobileApp;
use Microsoft\Graph\Generated\Models\AndroidMobileAppIdentifier;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new TargetAppsPostRequestBody();
$appsManagedMobileApp1 = new ManagedMobileApp();
$appsManagedMobileApp1->setOdataType('#microsoft.graph.managedMobileApp');
$appsManagedMobileApp1MobileAppIdentifier = new AndroidMobileAppIdentifier();
$appsManagedMobileApp1MobileAppIdentifier->setOdataType('microsoft.graph.androidMobileAppIdentifier');
$appsManagedMobileApp1MobileAppIdentifier->setPackageId('Package Id value');
$appsManagedMobileApp1->setMobileAppIdentifier($appsManagedMobileApp1MobileAppIdentifier);
$appsManagedMobileApp1->setId('0a129715-9715-0a12-1597-120a1597120a');
$appsManagedMobileApp1->setVersion('Version value');
$appsArray []= $appsManagedMobileApp1;
$requestBody->setApps($appsArray);


$graphServiceClient->deviceAppManagement()->managedAppPolicies()->byManagedAppPolicyId('managedAppPolicy-id')->targetApps()->post($requestBody)->wait();

```