---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\IdentityGovernance\LifecycleWorkflows\Workflows\Item\MicrosoftGraphIdentityGovernanceActivate\ActivatePostRequestBody;
use Microsoft\Graph\Generated\Models\User;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ActivatePostRequestBody();
$subjectsUser1 = new User();
$subjectsUser1->setId('8cdf25a8-c9d2-423e-a03d-3f39f03c3e97');
$subjectsArray []= $subjectsUser1;
$subjectsUser2 = new User();
$subjectsUser2->setId('ea09ac2e-77e3-4134-85f2-25ccf3c33387');
$subjectsArray []= $subjectsUser2;
$requestBody->setSubjects($subjectsArray);


$graphServiceClient->identityGovernance()->lifecycleWorkflows()->workflows()->byWorkflowId('workflow-id')->microsoftGraphIdentityGovernanceActivate()->post($requestBody)->wait();

```