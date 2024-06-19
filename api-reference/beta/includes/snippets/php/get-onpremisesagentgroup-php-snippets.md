---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\OnPremisesPublishingProfiles\Item\AgentGroups\Item\OnPremisesAgentGroupItemRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new OnPremisesAgentGroupItemRequestBuilderGetRequestConfiguration();
$queryParameters = OnPremisesAgentGroupItemRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->expand = ["publishedResources","agents"];
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->onPremisesPublishingProfiles()->byOnPremisesPublishingProfileId('onPremisesPublishingProfile-id')->agentGroups()->byOnPremisesAgentGroupId('onPremisesAgentGroup-id')->get($requestConfiguration)->wait();

```