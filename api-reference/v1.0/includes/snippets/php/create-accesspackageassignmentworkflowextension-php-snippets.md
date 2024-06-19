---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\CustomCalloutExtension;
use Microsoft\Graph\Generated\Models\AccessPackageAssignmentWorkflowExtension;
use Microsoft\Graph\Generated\Models\LogicAppTriggerEndpointConfiguration;
use Microsoft\Graph\Generated\Models\AzureAdPopTokenAuthentication;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CustomCalloutExtension();
$additionalData = [
	'value' => [
		'@odata.type' => '#microsoft.graph.accessPackageAssignmentWorkflowExtension',
		'displayName' => 'test_action_0127_email',
		'description' => 'this is for graph testing only',
		'endpointConfiguration' => [
			'@odata.type' => '#microsoft.graph.logicAppTriggerEndpointConfiguration',
			'subscriptionId' => '38ab2ccc-3747-4567-b36b-9478f5602f0d',
			'resourceGroupName' => 'test',
			'logicAppWorkflowName' => 'elm-extension-email',
		],
		'authenticationConfiguration' => [
			'@odata.type' => '#microsoft.graph.azureAdPopTokenAuthentication',
		],
	],
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->identityGovernance()->entitlementManagement()->catalogs()->byAccessPackageCatalogId('accessPackageCatalog-id')->customWorkflowExtensions()->post($requestBody)->wait();

```