---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Teams\Item\SendActivityNotification\SendActivityNotificationPostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\TeamworkActivityTopic;
use Microsoft\Graph\Beta\Generated\Models\TeamworkActivityTopicSource;
use Microsoft\Graph\Beta\Generated\Models\ItemBody;
use Microsoft\Graph\Beta\Generated\Models\TeamMembersNotificationRecipient;
use Microsoft\Graph\Beta\Generated\Models\KeyValuePair;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SendActivityNotificationPostRequestBody();
$topic = new TeamworkActivityTopic();
$topic->setSource(new TeamworkActivityTopicSource('entityUrl'));
$topic->setValue('https://graph.microsoft.com/beta/teams/e8bece96-d393-4b9b-b8da-69cedef1a7e7');
$requestBody->setTopic($topic);
$requestBody->setActivityType('pendingFinanceApprovalRequests');
$previewText = new ItemBody();
$previewText->setContent('Internal spending team has a pending finance approval requests');
$requestBody->setPreviewText($previewText);
$recipient = new TeamMembersNotificationRecipient();
$recipient->setOdataType('microsoft.graph.teamMembersNotificationRecipient');
$recipient->setTeamId('e8bece96-d393-4b9b-b8da-69cedef1a7e7');
$requestBody->setRecipient($recipient);
$templateParametersKeyValuePair1 = new KeyValuePair();
$templateParametersKeyValuePair1->setName('pendingRequestCount');
$templateParametersKeyValuePair1->setValue('5');
$templateParametersArray []= $templateParametersKeyValuePair1;
$requestBody->setTemplateParameters($templateParametersArray);


$graphServiceClient->teams()->byTeamId('team-id')->sendActivityNotification()->post($requestBody)->wait();

```