---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyConfigurationDefault;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyB2BSetting;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyTargetConfiguration;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyTargetConfigurationAccessType;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyTarget;
use Microsoft\Graph\Beta\Generated\Models\CrossTenantAccessPolicyTargetType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CrossTenantAccessPolicyConfigurationDefault();
$b2bCollaborationOutbound = new CrossTenantAccessPolicyB2BSetting();
$b2bCollaborationOutboundUsersAndGroups = new CrossTenantAccessPolicyTargetConfiguration();
$b2bCollaborationOutboundUsersAndGroups->setAccessType(new CrossTenantAccessPolicyTargetConfigurationAccessType('blocked'));
$targetsCrossTenantAccessPolicyTarget1 = new CrossTenantAccessPolicyTarget();
$targetsCrossTenantAccessPolicyTarget1->setTarget('0be493dc-cb56-4a53-936f-9cf64410b8b0');
$targetsCrossTenantAccessPolicyTarget1->setTargetType(new CrossTenantAccessPolicyTargetType('group'));
$targetsArray []= $targetsCrossTenantAccessPolicyTarget1;
$b2bCollaborationOutboundUsersAndGroups->setTargets($targetsArray);

$b2bCollaborationOutbound->setUsersAndGroups($b2bCollaborationOutboundUsersAndGroups);
$b2bCollaborationOutboundApplications = new CrossTenantAccessPolicyTargetConfiguration();
$b2bCollaborationOutboundApplications->setAccessType(new CrossTenantAccessPolicyTargetConfigurationAccessType('blocked'));
$targetsCrossTenantAccessPolicyTarget1 = new CrossTenantAccessPolicyTarget();
$targetsCrossTenantAccessPolicyTarget1->setTarget('AllApplications');
$targetsCrossTenantAccessPolicyTarget1->setTargetType(new CrossTenantAccessPolicyTargetType('application'));
$targetsArray []= $targetsCrossTenantAccessPolicyTarget1;
$b2bCollaborationOutboundApplications->setTargets($targetsArray);

$b2bCollaborationOutbound->setApplications($b2bCollaborationOutboundApplications);
$requestBody->setB2bCollaborationOutbound($b2bCollaborationOutbound);

$result = $graphServiceClient->policies()->crossTenantAccessPolicy()->escapedDefault()->patch($requestBody)->wait();

```