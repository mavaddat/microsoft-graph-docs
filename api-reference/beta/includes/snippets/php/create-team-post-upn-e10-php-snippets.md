---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Team;
use Microsoft\Graph\Beta\Generated\Models\ConversationMember;
use Microsoft\Graph\Beta\Generated\Models\AadUserConversationMember;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Team();
$requestBody->setDisplayName('My Sample Team');
$requestBody->setDescription('My Sample Team’s Description');
$membersConversationMember1 = new AadUserConversationMember();
$membersConversationMember1->setOdataType('#microsoft.graph.aadUserConversationMember');
$membersConversationMember1->setRoles(['owner', 	]);
$additionalData = [
	'user@odata.bind' => 'https://graph.microsoft.com/beta/users(\'jacob@contoso.com\')',
];
$membersConversationMember1->setAdditionalData($additionalData);
$membersArray []= $membersConversationMember1;
$requestBody->setMembers($membersArray);

$additionalData = [
'template@odata.bind' => 'https://graph.microsoft.com/beta/teamsTemplates(\'standard\')',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->teams()->post($requestBody)->wait();

```