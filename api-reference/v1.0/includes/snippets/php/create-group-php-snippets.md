---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Group;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Group();
$requestBody->setDescription('Self help community for library');
$requestBody->setDisplayName('Library Assist');
$requestBody->setGroupTypes(['Unified', 	]);
$requestBody->setMailEnabled(true);
$requestBody->setMailNickname('library');
$requestBody->setSecurityEnabled(false);

$result = $graphServiceClient->groups()->post($requestBody)->wait();

```