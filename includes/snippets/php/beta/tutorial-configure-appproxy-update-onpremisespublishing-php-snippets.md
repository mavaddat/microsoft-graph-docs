---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Application;
use Microsoft\Graph\Beta\Generated\Models\OnPremisesPublishing;
use Microsoft\Graph\Beta\Generated\Models\ExternalAuthenticationType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Application();
$onPremisesPublishing = new OnPremisesPublishing();
$onPremisesPublishing->setExternalAuthenticationType(new ExternalAuthenticationType('aadPreAuthentication'));
$onPremisesPublishing->setInternalUrl('https://contosoiwaapp.com');
$onPremisesPublishing->setExternalUrl('https://contosoiwaapp-contoso.msappproxy.net');
$onPremisesPublishing->setIsHttpOnlyCookieEnabled(true);
$onPremisesPublishing->setIsOnPremPublishingEnabled(true);
$onPremisesPublishing->setIsPersistentCookieEnabled(true);
$onPremisesPublishing->setIsSecureCookieEnabled(true);
$onPremisesPublishing->setIsStateSessionEnabled(true);
$onPremisesPublishing->setIsTranslateHostHeaderEnabled(true);
$onPremisesPublishing->setIsTranslateLinksInBodyEnabled(true);
$requestBody->setOnPremisesPublishing($onPremisesPublishing);

$result = $graphServiceClient->applications()->byApplicationId('application-id')->patch($requestBody)->wait();

```