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
$requestBody->setRoles(['owner', 	]);
$additionalData = [
	'user@odata.bind' => 'https://graph.microsoft.com/beta/users/8b081ef6-4792-4def-b2c9-c363a1bf41d5',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->chats()->byChatId('chat-id')->members()->post($requestBody)->wait();

```