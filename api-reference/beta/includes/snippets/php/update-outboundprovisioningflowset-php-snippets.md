---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\IndustryData\OutboundProvisioningFlowSet;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new OutboundProvisioningFlowSet();
$requestBody->setOdataType('#microsoft.graph.industryData.outboundProvisioningFlowSet');
$requestBody->setDisplayName('Outbound provisioning flow Updated');

$result = $graphServiceClient->external()->industryData()->outboundProvisioningFlowSets()->byOutboundProvisioningFlowSetId('outboundProvisioningFlowSet-id')->patch($requestBody)->wait();

```