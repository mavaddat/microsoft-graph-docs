---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$graphServiceClient->me()->profile()->anniversaries()->byPersonAnnualEventId('personAnnualEvent-id')->delete()->wait();

```