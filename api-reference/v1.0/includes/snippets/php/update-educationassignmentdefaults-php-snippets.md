---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\EducationAssignmentDefaults;
use Microsoft\Graph\Generated\Models\EducationAddedStudentAction;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new EducationAssignmentDefaults();
$requestBody->setAddedStudentAction(new EducationAddedStudentAction('assignIfOpen'));
$requestBody->setNotificationChannelUrl('https://graph.microsoft.com/beta/teams(\'acdefc6b-2dc6-4e71-b1e9-6d9810ab1793\')/channels(\'3da03fc4-8eac-4459-84fb-1422dc01f65e\')');

$result = $graphServiceClient->education()->classes()->byEducationClassId('educationClass-id')->assignmentDefaults()->patch($requestBody)->wait();

```