---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$graphServiceClient->directoryRoles()->byDirectoryRoleId('directoryRole-id')->members()->byDirectoryObjectId('directoryObject-id')->ref()->delete()->wait();

```