---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\ServicePrincipals\Item\AddKey\AddKeyPostRequestBody;
use Microsoft\Graph\Generated\Models\KeyCredential;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AddKeyPostRequestBody();
$keyCredential = new KeyCredential();
$keyCredential->setType('AsymmetricX509Cert');
$keyCredential->setUsage('Verify');
$keyCredential->setKey(\GuzzleHttp\Psr7\Utils::streamFor(base64_decode('MIIDYDCCAki...')));
$requestBody->setKeyCredential($keyCredential);
$requestBody->setPasswordCredential(null);
$requestBody->setProof('eyJ0eXAiOiJ...');

$result = $graphServiceClient->servicePrincipals()->byServicePrincipalId('servicePrincipal-id')->addKey()->post($requestBody)->wait();

```