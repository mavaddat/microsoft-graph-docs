---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\UnifiedRoleManagementPolicyExpirationRule;
use Microsoft\Graph\Beta\Generated\Models\UnifiedRoleManagementPolicyRuleTarget;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new UnifiedRoleManagementPolicyExpirationRule();
$requestBody->setOdataType('#microsoft.graph.unifiedRoleManagementPolicyExpirationRule');
$requestBody->setId('Expiration_EndUser_Assignment');
$requestBody->setIsExpirationRequired(true);
$requestBody->setMaximumDuration(new \DateInterval('PT1H45M'));
$target = new UnifiedRoleManagementPolicyRuleTarget();
$target->setOdataType('microsoft.graph.unifiedRoleManagementPolicyRuleTarget');
$target->setCaller('EndUser');
$target->setOperations(['All', 	]);
$target->setLevel('Assignment');
$target->setInheritableSettings([	]);
$target->setEnforcedSettings([	]);
$requestBody->setTarget($target);

$result = $graphServiceClient->policies()->roleManagementPolicies()->byUnifiedRoleManagementPolicyId('unifiedRoleManagementPolicy-id')->rules()->byUnifiedRoleManagementPolicyRuleId('unifiedRoleManagementPolicyRule-id')->patch($requestBody)->wait();

```