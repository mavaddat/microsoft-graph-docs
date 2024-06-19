---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Users\Item\Messages\Item\ReplyAll\ReplyAllPostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\Message;
use Microsoft\Graph\Beta\Generated\Models\Attachment;
use Microsoft\Graph\Beta\Generated\Models\FileAttachment;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ReplyAllPostRequestBody();
$message = new Message();
$attachmentsAttachment1 = new FileAttachment();
$attachmentsAttachment1->setOdataType('#microsoft.graph.fileAttachment');
$attachmentsAttachment1->setName('guidelines.txt');
$attachmentsAttachment1->setContentBytes(\GuzzleHttp\Psr7\Utils::streamFor(base64_decode('bWFjIGFuZCBjaGVlc2UgdG9kYXk=')));
$attachmentsArray []= $attachmentsAttachment1;
$message->setAttachments($attachmentsArray);

$requestBody->setMessage($message);
$requestBody->setComment('Please take a look at the attached guidelines before you decide on the name.');

$graphServiceClient->me()->messages()->byMessageId('message-id')->replyAll()->post($requestBody)->wait();

```