---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\AttributeSet;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AttributeSet();
$requestBody->setId('Engineering');
$requestBody->setDescription('Attributes for engineering team');
$requestBody->setMaxAttributesPerSet(25);

$result = $graphServiceClient->directory()->attributeSets()->post($requestBody)->wait();

```