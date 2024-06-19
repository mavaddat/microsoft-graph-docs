---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Chats\Item\SendActivityNotification\SendActivityNotificationPostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\TeamworkActivityTopic;
use Microsoft\Graph\Beta\Generated\Models\TeamworkActivityTopicSource;
use Microsoft\Graph\Beta\Generated\Models\ItemBody;
use Microsoft\Graph\Beta\Generated\Models\AadUserNotificationRecipient;
use Microsoft\Graph\Beta\Generated\Models\KeyValuePair;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SendActivityNotificationPostRequestBody();
$topic = new TeamworkActivityTopic();
$topic->setSource(new TeamworkActivityTopicSource('entityUrl'));
$topic->setValue('https://graph.microsoft.com/beta/chats/{chatId}/messages/{messageId}');
$requestBody->setTopic($topic);
$requestBody->setActivityType('approvalRequired');
$previewText = new ItemBody();
$previewText->setContent('Deployment requires your approval');
$requestBody->setPreviewText($previewText);
$recipient = new AadUserNotificationRecipient();
$recipient->setOdataType('microsoft.graph.aadUserNotificationRecipient');
$recipient->setUserId('jacob@contoso.com');
$requestBody->setRecipient($recipient);
$templateParametersKeyValuePair1 = new KeyValuePair();
$templateParametersKeyValuePair1->setName('approvalTaskId');
$templateParametersKeyValuePair1->setValue('2020AAGGTAPP');
$templateParametersArray []= $templateParametersKeyValuePair1;
$requestBody->setTemplateParameters($templateParametersArray);


$graphServiceClient->chats()->byChatId('chat-id')->sendActivityNotification()->post($requestBody)->wait();

```