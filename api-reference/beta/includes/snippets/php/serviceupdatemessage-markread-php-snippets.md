---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Admin\ServiceAnnouncement\Messages\MarkRead\MarkReadPostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new MarkReadPostRequestBody();
$requestBody->setMessageIds(['MC172851', 'MC167983', 	]);

$result = $graphServiceClient->admin()->serviceAnnouncement()->messages()->markRead()->post($requestBody)->wait();

```