---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\AadUserConversationMember;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AadUserConversationMember();
$requestBody->setOdataType('#microsoft.graph.aadUserConversationMember');
$requestBody->setRoles([	]);
$requestBody->setTenantId('a18103d1-a6ef-4f66-ac64-e4ef42ea8681');
$additionalData = [
	'user@odata.bind' => 'https://graph.microsoft.com/beta/users/bc3598dd-cce4-4742-ae15-173429951408',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->teams()->byTeamId('team-id')->channels()->byChannelId('channel-id')->members()->post($requestBody)->wait();

```