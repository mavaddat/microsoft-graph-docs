---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Security\Alerts\UpdateAlerts\UpdateAlertsPostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\Alert;
use Microsoft\Graph\Beta\Generated\Models\AlertFeedback;
use Microsoft\Graph\Beta\Generated\Models\AlertStatus;
use Microsoft\Graph\Beta\Generated\Models\SecurityVendorInformation;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new UpdateAlertsPostRequestBody();
$valueAlert1 = new Alert();
$valueAlert1->setAssignedTo('String');
$valueAlert1->setClosedDateTime(new \DateTime('String (timestamp)'));
$valueAlert1->setComments(['String', 	]);
$valueAlert1Feedback = new AlertFeedback();
$additionalData = [
	'@odata.type' => 'microsoft.graph.alertFeedback',
];
$valueAlert1Feedback->setAdditionalData($additionalData);
$valueAlert1->setFeedback($valueAlert1Feedback);
$valueAlert1->setId('String (identifier)');
$valueAlert1Status = new AlertStatus();
$additionalData = [
	'@odata.type' => 'microsoft.graph.alertStatus',
];
$valueAlert1Status->setAdditionalData($additionalData);
$valueAlert1->setStatus($valueAlert1Status);
$valueAlert1->setTags(['String', 	]);
$valueAlert1VendorInformation = new SecurityVendorInformation();
$valueAlert1VendorInformation->setProvider('String');
$valueAlert1VendorInformation->setVendor('String');
$valueAlert1->setVendorInformation($valueAlert1VendorInformation);
$valueArray []= $valueAlert1;
$requestBody->setValue($valueArray);


$result = $graphServiceClient->security()->alerts()->updateAlerts()->post($requestBody)->wait();

```