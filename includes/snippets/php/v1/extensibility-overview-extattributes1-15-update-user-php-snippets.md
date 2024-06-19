---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\User;
use Microsoft\Graph\Generated\Models\OnPremisesExtensionAttributes;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new User();
$onPremisesExtensionAttributes = new OnPremisesExtensionAttributes();
$onPremisesExtensionAttributes->setExtensionAttribute1('skypeId.adeleVance');
$onPremisesExtensionAttributes->setExtensionAttribute13(null);
$requestBody->setOnPremisesExtensionAttributes($onPremisesExtensionAttributes);

$result = $graphServiceClient->users()->byUserId('user-id')->patch($requestBody)->wait();

```