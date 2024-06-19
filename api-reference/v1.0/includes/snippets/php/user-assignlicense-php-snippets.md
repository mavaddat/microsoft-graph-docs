---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Users\Item\AssignLicense\AssignLicensePostRequestBody;
use Microsoft\Graph\Generated\Models\AssignedLicense;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AssignLicensePostRequestBody();
$addLicensesAssignedLicense1 = new AssignedLicense();
$addLicensesAssignedLicense1->setDisabledPlans(['11b0131d-43c8-4bbb-b2c8-e80f9a50834a', 	]);
$addLicensesAssignedLicense1->setSkuId('45715bb8-13f9-4bf6-927f-ef96c102d394');
$addLicensesArray []= $addLicensesAssignedLicense1;
$requestBody->setAddLicenses($addLicensesArray);

$requestBody->setRemoveLicenses(['bea13e0c-3828-4daa-a392-28af7ff61a0f', ]);

$result = $graphServiceClient->me()->assignLicense()->post($requestBody)->wait();

```