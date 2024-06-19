---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\ApprovalStage;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ApprovalStage();
$requestBody->setReviewResult('Approve');
$requestBody->setJustification('OK');

$result = $graphServiceClient->identityGovernance()->entitlementManagement()->accessPackageAssignmentApprovals()->byApprovalId('approval-id')->stages()->byApprovalStageId('approvalStage-id')->patch($requestBody)->wait();

```