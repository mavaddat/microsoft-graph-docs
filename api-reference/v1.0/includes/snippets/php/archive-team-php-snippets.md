---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Teams\Item\Archive\ArchivePostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ArchivePostRequestBody();

$graphServiceClient->teams()->byTeamId('team-id')->archive()->post($requestBody)->wait();

```