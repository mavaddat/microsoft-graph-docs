---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\DirectoryRole;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new DirectoryRole();
$requestBody->setRoleTemplateId('fe930be7-5e62-47db-91af-98c3a49a38b1');

$result = $graphServiceClient->directoryRoles()->post($requestBody)->wait();

```