---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Users\Item\GetMailTips\GetMailTipsPostRequestBody;
use Microsoft\Graph\Generated\Models\MailTipsType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new GetMailTipsPostRequestBody();
$requestBody->setEmailAddresses(['danas@contoso.com', 'fannyd@contoso.com', 	]);
$requestBody->setMailTipsOptions(new MailTipsType('automaticReplies, mailboxFullStatus'));

$result = $graphServiceClient->me()->getMailTips()->post($requestBody)->wait();

```