---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$result = $graphServiceClient->appCatalogs()->teamsApps()->byTeamsAppId('teamsApp-id')->appDefinitions()->byTeamsAppDefinitionId('teamsAppDefinition-id')->bot()->get()->wait();

```