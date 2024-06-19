---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\ServicePrincipals\Item\AddPassword\AddPasswordPostRequestBody;
use Microsoft\Graph\Generated\Models\PasswordCredential;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AddPasswordPostRequestBody();
$passwordCredential = new PasswordCredential();
$passwordCredential->setDisplayName('Password friendly name');
$requestBody->setPasswordCredential($passwordCredential);

$result = $graphServiceClient->servicePrincipals()->byServicePrincipalId('servicePrincipal-id')->addPassword()->post($requestBody)->wait();

```