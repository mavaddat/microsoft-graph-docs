---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Users\Item\Messages\Item\Forward\ForwardPostRequestBody;
use Microsoft\Graph\Generated\Models\Recipient;
use Microsoft\Graph\Generated\Models\EmailAddress;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ForwardPostRequestBody();
$requestBody->setComment('comment-value');
$toRecipientsRecipient1 = new Recipient();
$toRecipientsRecipient1EmailAddress = new EmailAddress();
$toRecipientsRecipient1EmailAddress->setName('name-value');
$toRecipientsRecipient1EmailAddress->setAddress('address-value');
$toRecipientsRecipient1->setEmailAddress($toRecipientsRecipient1EmailAddress);
$toRecipientsArray []= $toRecipientsRecipient1;
$requestBody->setToRecipients($toRecipientsArray);


$graphServiceClient->me()->messages()->byMessageId('message-id')->forward()->post($requestBody)->wait();

```