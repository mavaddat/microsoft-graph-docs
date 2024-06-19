---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\ExternalConnectors\Identity;
use Microsoft\Graph\Beta\Generated\Models\ExternalConnectors\IdentityType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Identity();
$requestBody->setId('e811976d-83df-4cbd-8b9b-5215b18aa874');
$requestBody->setType(new IdentityType('user'));

$result = $graphServiceClient->external()->connections()->byExternalConnectionId('externalConnection-id')->groups()->byExternalGroupId('externalGroup-id')->members()->post($requestBody)->wait();

```