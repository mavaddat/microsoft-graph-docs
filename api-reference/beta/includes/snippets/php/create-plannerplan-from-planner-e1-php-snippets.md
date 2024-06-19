---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\PlannerPlan;
use Microsoft\Graph\Beta\Generated\Models\PlannerPlanContainer;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new PlannerPlan();
$container = new PlannerPlanContainer();
$container->setUrl('https://graph.microsoft.com/beta/groups/ebf3b108-5234-4e22-b93d-656d7dae5874');
$requestBody->setContainer($container);
$requestBody->setTitle('title-value');

$result = $graphServiceClient->planner()->plans()->post($requestBody)->wait();

```