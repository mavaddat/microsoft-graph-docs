---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Application;
use Microsoft\Graph\Generated\Models\KeyCredential;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Application();
$keyCredentialsKeyCredential1 = new KeyCredential();
$keyCredentialsKeyCredential1->setEndDateTime(new \DateTime('2024-01-11T15:31:26Z'));
$keyCredentialsKeyCredential1->setStartDateTime(new \DateTime('2023-01-12T15:31:26Z'));
$keyCredentialsKeyCredential1->setType('AsymmetricX509Cert');
$keyCredentialsKeyCredential1->setUsage('Verify');
$keyCredentialsKeyCredential1->setKey(\GuzzleHttp\Psr7\Utils::streamFor(base64_decode('base64MIIDADCCAeigAwIBAgIQP6HEGDdZ65xJTcK4dCBvZzANBgkqhkiG9w0BAQsFADATMREwDwYDVQQDDAgyMDIzMDExMjAeFw0yMzAxMTIwODExNTZaFw0yNDAxMTIwODMxNTZaMBMxETAPBgNVBAMMCDIwMjMwMTEyMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAseKf1weEacJ67D6/...laxQPUbuIL+DaXVkKRm1V3GgIpKTBqMzTf4tCpy7rpUZbhcwAFw6h9A==')));
$keyCredentialsKeyCredential1->setDisplayName('CN=20230112');
$keyCredentialsArray []= $keyCredentialsKeyCredential1;
$requestBody->setKeyCredentials($keyCredentialsArray);


$result = $graphServiceClient->applications()->byApplicationId('application-id')->patch($requestBody)->wait();

```