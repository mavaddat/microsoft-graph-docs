---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Ediscovery\LegalHold;
use Microsoft\Graph\Beta\Generated\Models\IdentitySet;
use Microsoft\Graph\Beta\Generated\Models\Ediscovery\LegalHoldStatus;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new LegalHold();
$requestBody->setOdataType('#microsoft.graph.ediscovery.legalHold');
$requestBody->setDescription('String');
$createdBy = new IdentitySet();
$createdBy->setOdataType('microsoft.graph.identitySet');
$requestBody->setCreatedBy($createdBy);
$requestBody->setIsEnabled(boolean);
$requestBody->setStatus(new LegalHoldStatus('string'));
$requestBody->setContentQuery('String');
$requestBody->setErrors(['String', 	]);
$requestBody->setDisplayName('String');

$result = $graphServiceClient->compliance()->ediscovery()->cases()->byCaseId('case-id')->legalHolds()->post($requestBody)->wait();

```