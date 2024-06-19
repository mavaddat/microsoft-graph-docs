---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Simulation;
use Microsoft\Graph\Beta\Generated\Models\SimulationAttackTechnique;
use Microsoft\Graph\Beta\Generated\Models\SimulationAttackType;
use Microsoft\Graph\Beta\Generated\Models\SimulationStatus;
use Microsoft\Graph\Beta\Generated\Models\AddressBookAccountTargetContent;
use Microsoft\Graph\Beta\Generated\Models\AccountTargetContentType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Simulation();
$requestBody->setId('2f5548d1-0dd8-4cc8-9de0-e0d6ec7ea3dc');
$requestBody->setDisplayName('Graph Simulation');
$requestBody->setDurationInDays(7);
$requestBody->setAttackTechnique(new SimulationAttackTechnique('credentialHarvesting'));
$requestBody->setAttackType(new SimulationAttackType('social'));
$requestBody->setStatus(new SimulationStatus('scheduled'));
$includedAccountTarget = new AddressBookAccountTargetContent();
$includedAccountTarget->setOdataType('#microsoft.graph.addressBookAccountTargetContent');
$includedAccountTarget->setType(new AccountTargetContentType('addressBook'));
$includedAccountTarget->setAccountTargetEmails(['faiza@contoso.com', 	]);
$requestBody->setIncludedAccountTarget($includedAccountTarget);
$excludedAccountTarget = new AddressBookAccountTargetContent();
$excludedAccountTarget->setOdataType('#microsoft.graph.addressBookAccountTargetContent');
$excludedAccountTarget->setType(new AccountTargetContentType('addressBook'));
$excludedAccountTarget->setAccountTargetEmails(['sam@contoso.com', 	]);
$requestBody->setExcludedAccountTarget($excludedAccountTarget);
$additionalData = [
	'@odata.etag' => '\"0100aa9b-0000-0100-0000-6396fa270000\"',
	'payload@odata.bind' => 'https://graph.microsoft.com/beta/security/attacksimulation/payloads/12345678-9abc-def0-123456789a',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->security()->attackSimulation()->simulations()->bySimulationId('simulation-id')->patch($requestBody)->wait();

```