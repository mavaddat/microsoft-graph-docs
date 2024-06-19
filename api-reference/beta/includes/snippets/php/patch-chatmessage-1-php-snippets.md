---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\ChatMessage;
use Microsoft\Graph\Beta\Generated\Models\ChatMessageType;
use Microsoft\Graph\Beta\Generated\Models\ChatMessageImportance;
use Microsoft\Graph\Beta\Generated\Models\ChatMessageFromIdentitySet;
use Microsoft\Graph\Beta\Generated\Models\Identity;
use Microsoft\Graph\Beta\Generated\Models\ItemBody;
use Microsoft\Graph\Beta\Generated\Models\BodyType;
use Microsoft\Graph\Beta\Generated\Models\ChatMessageAttachment;
use Microsoft\Graph\Beta\Generated\Models\ChatMessageMention;
use Microsoft\Graph\Beta\Generated\Models\ChatMessageReaction;
use Microsoft\Graph\Beta\Generated\Models\ChatMessageHistoryItem;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ChatMessage();
$requestBody->setMessageType(new ChatMessageType('message'));
$requestBody->setSubject(null);
$requestBody->setSummary(null);
$requestBody->setImportance(new ChatMessageImportance('normal'));
$requestBody->setLocale('en-us');
$from = new ChatMessageFromIdentitySet();
$from->setApplication(null);
$from->setDevice(null);
$fromUser = new Identity();
$fromUser->setId('3b102402-813e-4e17-a6b2-f841aef1fdfc');
$fromUser->setDisplayName('Sumit Gupta');
$additionalData = [
	'userIdentityType' => 'aadUser',
];
$fromUser->setAdditionalData($additionalData);
$from->setUser($fromUser);
$additionalData = [
	'conversation' => null,
];
$from->setAdditionalData($additionalData);
$requestBody->setFrom($from);
$body = new ItemBody();
$body->setContentType(new BodyType('text'));
$body->setContent('Edit text only');
$requestBody->setBody($body);
$requestBody->setAttachments([	]);
$requestBody->setMentions([	]);
$requestBody->setReactions([	]);
$requestBody->setMessageHistory([	]);

$result = $graphServiceClient->teams()->byTeamId('team-id')->channels()->byChannelId('channel-id')->messages()->byChatMessageId('chatMessage-id')->patch($requestBody)->wait();

```