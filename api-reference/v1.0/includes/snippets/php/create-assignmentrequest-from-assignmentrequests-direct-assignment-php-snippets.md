---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\AccessPackageAssignmentRequest;
use Microsoft\Graph\Generated\Models\AccessPackageRequestType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AccessPackageAssignmentRequest();
$requestBody->setRequestType(new AccessPackageRequestType('adminAdd'));
$additionalData = [
	'accessPackageAssignment' => [
		'target' => [
			'email' => 'user@contoso.com',
		],
		'assignmentPolicyId' => '2264bf65-76ba-417b-a27d-54d291f0cbc8',
		'accessPackageId' => 'a914b616-e04e-476b-aa37-91038f0b165b',
	],
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->identityGovernance()->entitlementManagement()->assignmentRequests()->post($requestBody)->wait();

```