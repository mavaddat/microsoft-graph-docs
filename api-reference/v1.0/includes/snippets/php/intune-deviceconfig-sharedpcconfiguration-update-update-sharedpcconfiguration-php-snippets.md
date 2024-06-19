---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\SharedPCConfiguration;
use Microsoft\Graph\Generated\Models\SharedPCAccountManagerPolicy;
use Microsoft\Graph\Generated\Models\SharedPCAccountDeletionPolicyType;
use Microsoft\Graph\Generated\Models\SharedPCAllowedAccountType;
use Microsoft\Kiota\Abstractions\Types\Time;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SharedPCConfiguration();
$requestBody->setOdataType('#microsoft.graph.sharedPCConfiguration');
$requestBody->setDescription('Description value');
$requestBody->setDisplayName('Display Name value');
$requestBody->setVersion(7);
$accountManagerPolicy = new SharedPCAccountManagerPolicy();
$accountManagerPolicy->setOdataType('microsoft.graph.sharedPCAccountManagerPolicy');
$accountManagerPolicy->setAccountDeletionPolicy(new SharedPCAccountDeletionPolicyType('diskSpaceThreshold'));
$accountManagerPolicy->setCacheAccountsAboveDiskFreePercentage(4);
$accountManagerPolicy->setInactiveThresholdDays(5);
$accountManagerPolicy->setRemoveAccountsBelowDiskFreePercentage(5);
$requestBody->setAccountManagerPolicy($accountManagerPolicy);
$requestBody->setAllowedAccounts(new SharedPCAllowedAccountType('domain'));
$requestBody->setAllowLocalStorage(true);
$requestBody->setDisableAccountManager(true);
$requestBody->setDisableEduPolicies(true);
$requestBody->setDisablePowerPolicies(true);
$requestBody->setDisableSignInOnResume(true);
$requestBody->setEnabled(true);
$requestBody->setIdleTimeBeforeSleepInSeconds(12);
$requestBody->setKioskAppDisplayName('Kiosk App Display Name value');
$requestBody->setKioskAppUserModelId('Kiosk App User Model Id value');
$requestBody->setMaintenanceStartTime(new Time('11:59:24.7240000'));

$result = $graphServiceClient->deviceManagement()->deviceConfigurations()->byDeviceConfigurationId('deviceConfiguration-id')->patch($requestBody)->wait();

```