---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\EducationGradingScheme;
use Microsoft\Graph\Beta\Generated\Models\EducationGradingSchemeGrade;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new EducationGradingScheme();
$requestBody->setDisplayName('New name 02');
$gradesEducationGradingSchemeGrade1 = new EducationGradingSchemeGrade();
$gradesEducationGradingSchemeGrade1->setDisplayName('Only grade');
$gradesEducationGradingSchemeGrade1->setMinPercentage(0);
$gradesArray []= $gradesEducationGradingSchemeGrade1;
$requestBody->setGrades($gradesArray);


$result = $graphServiceClient->education()->classes()->byEducationClassId('educationClass-id')->assignmentSettings()->gradingSchemes()->post($requestBody)->wait();

```