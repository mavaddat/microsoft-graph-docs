---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\ConversationThread;
use Microsoft\Graph\Generated\Models\Post;
use Microsoft\Graph\Generated\Models\ItemBody;
use Microsoft\Graph\Generated\Models\BodyType;
use Microsoft\Graph\Generated\Models\Recipient;
use Microsoft\Graph\Generated\Models\EmailAddress;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ConversationThread();
$requestBody->setTopic('New Conversation Thread Topic');
$postsPost1 = new Post();
$postsPost1Body = new ItemBody();
$postsPost1Body->setContentType(new BodyType('html'));
$postsPost1Body->setContent('this is body content');
$postsPost1->setBody($postsPost1Body);
$newParticipantsRecipient1 = new Recipient();
$newParticipantsRecipient1EmailAddress = new EmailAddress();
$newParticipantsRecipient1EmailAddress->setName('Alex Darrow');
$newParticipantsRecipient1EmailAddress->setAddress('alexd@contoso.com');
$newParticipantsRecipient1->setEmailAddress($newParticipantsRecipient1EmailAddress);
$newParticipantsArray []= $newParticipantsRecipient1;
$postsPost1->setNewParticipants($newParticipantsArray);

$postsArray []= $postsPost1;
$requestBody->setPosts($postsArray);


$result = $graphServiceClient->groups()->byGroupId('group-id')->threads()->post($requestBody)->wait();

```