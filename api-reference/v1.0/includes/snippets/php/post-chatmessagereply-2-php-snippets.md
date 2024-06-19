---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\ChatMessage;
use Microsoft\Graph\Generated\Models\ChatMessageFromIdentitySet;
use Microsoft\Graph\Generated\Models\Identity;
use Microsoft\Graph\Generated\Models\ItemBody;
use Microsoft\Graph\Generated\Models\BodyType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ChatMessage();
$requestBody->setCreatedDateTime(new \DateTime('2019-02-04T19:58:15.511Z'));
$from = new ChatMessageFromIdentitySet();
$fromUser = new Identity();
$fromUser->setId('8c0a1a67-50ce-4114-bb6c-da9c5dbcf6ca');
$fromUser->setDisplayName('John Doe');
$from->setUser($fromUser);
$requestBody->setFrom($from);
$body = new ItemBody();
$body->setContentType(new BodyType('html'));
$body->setContent('Hello World');
$requestBody->setBody($body);

$result = $graphServiceClient->teams()->byTeamId('team-id')->channels()->byChannelId('channel-id')->messages()->byChatMessageId('chatMessage-id')->replies()->post($requestBody)->wait();

```