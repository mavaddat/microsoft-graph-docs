---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\SchedulingGroup;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SchedulingGroup();
$requestBody->setDisplayName('Cashiers');
$requestBody->setIsActive(true);
$requestBody->setCode('CashierCode');
$requestBody->setUserIds(['c5d0c76b-80c4-481c-be50-923cd8d680a1', '2a4296b3-a28a-44ba-bc66-0274b9b95851', 	]);

$result = $graphServiceClient->teams()->byTeamId('team-id')->schedule()->schedulingGroups()->post($requestBody)->wait();

```