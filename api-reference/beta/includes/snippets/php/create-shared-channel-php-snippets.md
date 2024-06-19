---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Channel;
use Microsoft\Graph\Beta\Generated\Models\ChannelMembershipType;
use Microsoft\Graph\Beta\Generated\Models\ConversationMember;
use Microsoft\Graph\Beta\Generated\Models\AadUserConversationMember;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Channel();
$requestBody->setDisplayName('My First Shared Channel');
$requestBody->setDescription('This is my first shared channel');
$requestBody->setMembershipType(new ChannelMembershipType('shared'));
$membersConversationMember1 = new AadUserConversationMember();
$membersConversationMember1->setOdataType('#microsoft.graph.aadUserConversationMember');
$membersConversationMember1->setRoles(['owner', 	]);
$additionalData = [
	'user@odata.bind' => 'https://graph.microsoft.com/beta/users(\'7640023f-fe43-gv3f-9gg4-84a9efe4acd6\')',
];
$membersConversationMember1->setAdditionalData($additionalData);
$membersArray []= $membersConversationMember1;
$requestBody->setMembers($membersArray);


$result = $graphServiceClient->teams()->byTeamId('team-id')->channels()->post($requestBody)->wait();

```