---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Users\Item\Events\Item\Attachments\CreateUploadSession\CreateUploadSessionPostRequestBody;
use Microsoft\Graph\Generated\Models\AttachmentItem;
use Microsoft\Graph\Generated\Models\AttachmentType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CreateUploadSessionPostRequestBody();
$attachmentItem = new AttachmentItem();
$attachmentItem->setAttachmentType(new AttachmentType('file'));
$attachmentItem->setName('flower');
$attachmentItem->setSize(3483322);
$requestBody->setAttachmentItem($attachmentItem);

$result = $graphServiceClient->me()->events()->byEventId('event-id')->attachments()->createUploadSession()->post($requestBody)->wait();

```