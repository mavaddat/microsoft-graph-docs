---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$result = $graphServiceClient->roleManagement()->exchange()->roleDefinitions()->byUnifiedRoleDefinitionId('unifiedRoleDefinition-id')->get()->wait();

```