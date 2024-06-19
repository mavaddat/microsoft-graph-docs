---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\CalendarPermission;
use Microsoft\Graph\Generated\Models\CalendarRoleType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CalendarPermission();
$requestBody->setRole(new CalendarRoleType('write'));

$result = $graphServiceClient->users()->byUserId('user-id')->calendar()->calendarPermissions()->byCalendarPermissionId('calendarPermission-id')->patch($requestBody)->wait();

```