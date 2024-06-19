---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Groups\Item\AssignLicense\AssignLicensePostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\AssignedLicense;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AssignLicensePostRequestBody();
$requestBody->setAddLicenses([	]);
$requestBody->setRemoveLicenses(['c7df2760-2c81-4ef7-b578-5b5392b571df', 'b05e124f-c7cc-45a0-a6aa-8cf78c946968', 	]);

$result = $graphServiceClient->groups()->byGroupId('group-id')->assignLicense()->post($requestBody)->wait();

```