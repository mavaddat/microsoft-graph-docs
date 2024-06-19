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
$requestBody->setId('e5477431-1038-484e-bf69-1dfedb97a110');
$requestBody->setType(new IdentityType('externalGroup'));

$result = $graphServiceClient->external()->connections()->byExternalConnectionId('externalConnection-id')->groups()->byExternalGroupId('externalGroup-id')->members()->post($requestBody)->wait();

```