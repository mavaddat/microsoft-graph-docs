---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\TrustFramework\KeySets\Item\GenerateKey\GenerateKeyPostRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new GenerateKeyPostRequestBody();
$requestBody->setEscapedUse('sig');
$requestBody->setKty('RSA');
$requestBody->setNbf(1508969811);
$requestBody->setExp(1508969811);

$result = $graphServiceClient->trustFramework()->keySets()->byTrustFrameworkKeySetId('trustFrameworkKeySet-id')->generateKey()->post($requestBody)->wait();

```