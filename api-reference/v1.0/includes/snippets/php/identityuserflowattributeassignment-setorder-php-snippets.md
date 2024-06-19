---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Identity\B2xUserFlows\Item\UserAttributeAssignments\SetOrder\SetOrderPostRequestBody;
use Microsoft\Graph\Generated\Models\AssignmentOrder;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SetOrderPostRequestBody();
$newAssignmentOrder = new AssignmentOrder();
$newAssignmentOrder->setOrder(['City', 'extension_GUID_ShoeSize', 	]);
$requestBody->setNewAssignmentOrder($newAssignmentOrder);

$graphServiceClient->identity()->b2xUserFlows()->byB2xIdentityUserFlowId('b2xIdentityUserFlow-id')->userAttributeAssignments()->setOrder()->post($requestBody)->wait();

```