---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Sites\Item\Lists\Item\ContentTypes\AddCopy\AddCopyPostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AddCopyPostRequestBody();
$requestBody->setContentType('https://graph.microsoft.com/beta/sites/id/contentTypes/0x0101');

$result = $graphServiceClient->sites()->bySiteId('site-id')->lists()->byListId('list-id')->contentTypes()->addCopy()->post($requestBody)->wait();

```