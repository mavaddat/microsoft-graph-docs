---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\EducationSchool;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new EducationSchool();
$requestBody->setDisplayName('Fabrikam Arts High School');
$requestBody->setDescription('Magnate school for the arts. Los Angeles School District');

$result = $graphServiceClient->education()->schools()->byEducationSchoolId('educationSchool-id')->patch($requestBody)->wait();

```