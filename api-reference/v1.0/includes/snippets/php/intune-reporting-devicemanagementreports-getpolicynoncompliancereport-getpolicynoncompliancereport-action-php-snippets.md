---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\DeviceManagement\Reports\GetPolicyNonComplianceReport\GetPolicyNonComplianceReportPostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new GetPolicyNonComplianceReportPostRequestBody();
$requestBody->setName('Name value');
$requestBody->setSelect(['Select value', 	]);
$requestBody->setSearch('Search value');
$requestBody->setGroupBy(['Group By value', 	]);
$requestBody->setOrderBy(['Order By value', 	]);
$requestBody->setSkip(4);
$requestBody->setTop(3);
$requestBody->setSessionId('Session Id value');
$requestBody->setFilter('Filter value');

$graphServiceClient->deviceManagement()->reports()->getPolicyNonComplianceReport()->post($requestBody)->wait();

```