---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Users\Item\Teamwork\InstalledApps\Item\UserScopeTeamsAppInstallationItemRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new UserScopeTeamsAppInstallationItemRequestBuilderGetRequestConfiguration();
$queryParameters = UserScopeTeamsAppInstallationItemRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->expand = ["teamsAppDefinition"];
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->users()->byUserId('user-id')->teamwork()->installedApps()->byUserScopeTeamsAppInstallationId('userScopeTeamsAppInstallation-id')->get($requestConfiguration)->wait();

```