---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Ediscovery\UnifiedGroupSource;
use Microsoft\Graph\Beta\Generated\Models\Ediscovery\SourceType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new UnifiedGroupSource();
$requestBody->setIncludedSources(new SourceType('mailbox, site'));
$additionalData = [
	'group@odata.bind' => 'https://graph.microsoft.com/v1.0/groups/b96f95c5-b1b3-4142-b039-8ac79e7d2c84',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->compliance()->ediscovery()->cases()->byCaseId('case-id')->custodians()->byCustodianId('custodian-id')->unifiedGroupSources()->post($requestBody)->wait();

```