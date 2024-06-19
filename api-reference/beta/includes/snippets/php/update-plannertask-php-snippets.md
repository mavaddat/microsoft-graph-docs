---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Planner\Tasks\Item\PlannerTaskItemRequestBuilderPatchRequestConfiguration;
use Microsoft\Graph\Beta\Generated\Models\PlannerTask;
use Microsoft\Graph\Beta\Generated\Models\PlannerAssignments;
use Microsoft\Graph\Beta\Generated\Models\PlannerAssignment;
use Microsoft\Graph\Beta\Generated\Models\PlannerAppliedCategories;
use Microsoft\Graph\Beta\Generated\Models\PlannerTaskRecurrence;
use Microsoft\Graph\Beta\Generated\Models\PlannerRecurrenceSchedule;
use Microsoft\Graph\Beta\Generated\Models\RecurrencePattern;
use Microsoft\Graph\Beta\Generated\Models\RecurrencePatternType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new PlannerTask();
$assignments = new PlannerAssignments();
$additionalData = [
	'fbab97d0-4932-4511-b675-204639209557' => [
		'@odata.type' => '#microsoft.graph.plannerAssignment',
		'orderHint' => 'N9917 U2883!',
	],
];
$assignments->setAdditionalData($additionalData);
$requestBody->setAssignments($assignments);
$appliedCategories = new PlannerAppliedCategories();
$additionalData = [
	'category3' => true,
	'category4' => false,
];
$appliedCategories->setAdditionalData($additionalData);
$requestBody->setAppliedCategories($appliedCategories);
$recurrence = new PlannerTaskRecurrence();
$recurrenceSchedule = new PlannerRecurrenceSchedule();
$recurrenceSchedulePattern = new RecurrencePattern();
$recurrenceSchedulePattern->setType(new RecurrencePatternType('daily'));
$recurrenceSchedulePattern->setInterval(3);
$recurrenceSchedule->setPattern($recurrenceSchedulePattern);
$recurrenceSchedule->setPatternStartDateTime(new \DateTime('2022-02-22T02:10:33Z'));
$recurrence->setSchedule($recurrenceSchedule);
$requestBody->setRecurrence($recurrence);
$requestConfiguration = new PlannerTaskItemRequestBuilderPatchRequestConfiguration();
$headers = [
		'Prefer' => 'return=representation',
		'If-Match' => 'W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="',
	];
$requestConfiguration->headers = $headers;


$result = $graphServiceClient->planner()->tasks()->byPlannerTaskId('plannerTask-id')->patch($requestBody, $requestConfiguration)->wait();

```