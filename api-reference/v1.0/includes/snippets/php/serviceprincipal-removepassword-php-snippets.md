---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\ServicePrincipals\Item\RemovePassword\RemovePasswordPostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new RemovePasswordPostRequestBody();
$requestBody->setKeyId('f0b0b335-1d71-4883-8f98-567911bfdca6');

$graphServiceClient->servicePrincipals()->byServicePrincipalId('servicePrincipal-id')->removePassword()->post($requestBody)->wait();

```