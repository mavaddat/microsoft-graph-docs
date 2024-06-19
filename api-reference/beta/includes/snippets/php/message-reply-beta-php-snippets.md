---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Users\Item\Messages\Item\Reply\ReplyPostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\Message;
use Microsoft\Graph\Beta\Generated\Models\Recipient;
use Microsoft\Graph\Beta\Generated\Models\EmailAddress;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ReplyPostRequestBody();
$message = new Message();
$toRecipientsRecipient1 = new Recipient();
$toRecipientsRecipient1EmailAddress = new EmailAddress();
$toRecipientsRecipient1EmailAddress->setAddress('samanthab@contoso.com');
$toRecipientsRecipient1EmailAddress->setName('Samantha Booth');
$toRecipientsRecipient1->setEmailAddress($toRecipientsRecipient1EmailAddress);
$toRecipientsArray []= $toRecipientsRecipient1;
$toRecipientsRecipient2 = new Recipient();
$toRecipientsRecipient2EmailAddress = new EmailAddress();
$toRecipientsRecipient2EmailAddress->setAddress('randiw@contoso.com');
$toRecipientsRecipient2EmailAddress->setName('Randi Welch');
$toRecipientsRecipient2->setEmailAddress($toRecipientsRecipient2EmailAddress);
$toRecipientsArray []= $toRecipientsRecipient2;
$message->setToRecipients($toRecipientsArray);

$requestBody->setMessage($message);
$requestBody->setComment('Samantha, Randi, would you name the group please?');

$graphServiceClient->me()->messages()->byMessageId('message-id')->reply()->post($requestBody)->wait();

```