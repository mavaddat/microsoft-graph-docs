---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\AuthenticationFlowsPolicy;
use Microsoft\Graph\Beta\Generated\Models\SelfServiceSignUpAuthenticationFlowConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AuthenticationFlowsPolicy();
$selfServiceSignUp = new SelfServiceSignUpAuthenticationFlowConfiguration();
$selfServiceSignUp->setIsEnabled(true);
$requestBody->setSelfServiceSignUp($selfServiceSignUp);

$result = $graphServiceClient->policies()->authenticationFlowsPolicy()->patch($requestBody)->wait();

```