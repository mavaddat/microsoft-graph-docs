---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Applications\Item\AddKey\AddKeyPostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\KeyCredential;
use Microsoft\Graph\Beta\Generated\Models\PasswordCredential;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AddKeyPostRequestBody();
$keyCredential = new KeyCredential();
$keyCredential->setType('X509CertAndPassword');
$keyCredential->setUsage('Sign');
$keyCredential->setKey(\GuzzleHttp\Psr7\Utils::streamFor(base64_decode('MIIDYDCCAki...')));
$requestBody->setKeyCredential($keyCredential);
$passwordCredential = new PasswordCredential();
$passwordCredential->setSecretText('MKTr0w1...');
$requestBody->setPasswordCredential($passwordCredential);
$requestBody->setProof('eyJ0eXAiOiJ...');

$result = $graphServiceClient->applications()->byApplicationId('application-id')->addKey()->post($requestBody)->wait();

```