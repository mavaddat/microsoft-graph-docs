---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\WorkforceIntegration;
use Microsoft\Graph\Beta\Generated\Models\WorkforceIntegrationEncryption;
use Microsoft\Graph\Beta\Generated\Models\WorkforceIntegrationEncryptionProtocol;
use Microsoft\Graph\Beta\Generated\Models\WorkforceIntegrationSupportedEntities;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new WorkforceIntegration();
$requestBody->setDisplayName('displayName-value');
$requestBody->setApiVersion(99);
$encryption = new WorkforceIntegrationEncryption();
$encryption->setProtocol(new WorkforceIntegrationEncryptionProtocol('protocol-value'));
$encryption->setSecret('secret-value');
$requestBody->setEncryption($encryption);
$requestBody->setIsActive(true);
$requestBody->setUrl('url-value');
$requestBody->setSupports(new WorkforceIntegrationSupportedEntities('supports-value'));

$result = $graphServiceClient->teamwork()->workforceIntegrations()->post($requestBody)->wait();

```