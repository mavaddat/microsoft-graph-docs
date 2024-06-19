---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Event;
use Microsoft\Graph\Beta\Generated\Models\ItemBody;
use Microsoft\Graph\Beta\Generated\Models\BodyType;
use Microsoft\Graph\Beta\Generated\Models\DateTimeTimeZone;
use Microsoft\Graph\Beta\Generated\Models\Location;
use Microsoft\Graph\Beta\Generated\Models\Attendee;
use Microsoft\Graph\Beta\Generated\Models\EmailAddress;
use Microsoft\Graph\Beta\Generated\Models\AttendeeType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Event();
$requestBody->setSubject('Let\'s go for lunch');
$body = new ItemBody();
$body->setContentType(new BodyType('hTML'));
$body->setContent('Does late morning work for you?');
$requestBody->setBody($body);
$start = new DateTimeTimeZone();
$start->setDateTime('2019-06-15T12:00:00');
$start->setTimeZone('Pacific Standard Time');
$requestBody->setStart($start);
$end = new DateTimeTimeZone();
$end->setDateTime('2019-06-15T14:00:00');
$end->setTimeZone('Pacific Standard Time');
$requestBody->setEnd($end);
$location = new Location();
$location->setDisplayName('Harry\'s Bar');
$requestBody->setLocation($location);
$attendeesAttendee1 = new Attendee();
$attendeesAttendee1EmailAddress = new EmailAddress();
$attendeesAttendee1EmailAddress->setAddress('adelev@contoso.com');
$attendeesAttendee1EmailAddress->setName('Adele Vance');
$attendeesAttendee1->setEmailAddress($attendeesAttendee1EmailAddress);
$attendeesAttendee1->setType(new AttendeeType('required'));
$attendeesArray []= $attendeesAttendee1;
$requestBody->setAttendees($attendeesArray);


$result = $graphServiceClient->groups()->byGroupId('group-id')->events()->post($requestBody)->wait();

```