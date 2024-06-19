---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\IdentityGovernance\EntitlementManagement\AccessPackageAssignmentPolicies\Item\AccessPackageAssignmentPolicyItemRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new AccessPackageAssignmentPolicyItemRequestBuilderGetRequestConfiguration();
$queryParameters = AccessPackageAssignmentPolicyItemRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->expand = ["customExtensionHandlers(\$expand=customExtension)"];
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->identityGovernance()->entitlementManagement()->accessPackageAssignmentPolicies()->byAccessPackageAssignmentPolicyId('accessPackageAssignmentPolicy-id')->get($requestConfiguration)->wait();

```