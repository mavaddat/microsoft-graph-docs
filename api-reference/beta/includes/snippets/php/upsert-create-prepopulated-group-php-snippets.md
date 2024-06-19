---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Group;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Group();
$requestBody->setDescription('Group with designated owner and members');
$requestBody->setDisplayName('Operations group');
$requestBody->setGroupTypes([	]);
$requestBody->setMailEnabled(false);
$requestBody->setMailNickname('operations2019');
$requestBody->setSecurityEnabled(true);
$additionalData = [
	'owners@odata.bind' => [
'https://graph.microsoft.com/beta/users/26be1845-4119-4801-a799-aea79d09f1a2', ],
	'members@odata.bind' => [
'https://graph.microsoft.com/beta/users/ff7cb387-6688-423c-8188-3da9532a73cc', 'https://graph.microsoft.com/beta/users/69456242-0067-49d3-ba96-9de6f2728e14', ],
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->groupsWithUniqueName('{uniqueName}', )->patch($requestBody)->wait();

```