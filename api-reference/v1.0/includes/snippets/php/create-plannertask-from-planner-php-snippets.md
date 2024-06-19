---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\PlannerTask;
use Microsoft\Graph\Generated\Models\PlannerAssignments;
use Microsoft\Graph\Generated\Models\PlannerAssignment;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new PlannerTask();
$requestBody->setPlanId('xqQg5FS2LkCp935s-FIFm2QAFkHM');
$requestBody->setBucketId('hsOf2dhOJkqyYYZEtdzDe2QAIUCR');
$requestBody->setTitle('Update client list');
$assignments = new PlannerAssignments();
$additionalData = [
	'fbab97d0-4932-4511-b675-204639209557' => [
		'@odata.type' => '#microsoft.graph.plannerAssignment',
		'orderHint' => ' !',
	],
];
$assignments->setAdditionalData($additionalData);
$requestBody->setAssignments($assignments);

$result = $graphServiceClient->planner()->tasks()->post($requestBody)->wait();

```