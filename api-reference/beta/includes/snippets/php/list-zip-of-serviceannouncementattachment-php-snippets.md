---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$graphServiceClient->admin()->serviceAnnouncement()->messages()->byServiceUpdateMessageId('serviceUpdateMessage-id')->attachmentsArchive()->get()->wait();

```