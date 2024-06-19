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
use Microsoft\Graph\Beta\Generated\Models\PatternedRecurrence;
use Microsoft\Graph\Beta\Generated\Models\RecurrencePattern;
use Microsoft\Graph\Beta\Generated\Models\RecurrencePatternType;
use Microsoft\Graph\Beta\Generated\Models\DayOfWeek;
use Microsoft\Graph\Beta\Generated\Models\RecurrenceRange;
use Microsoft\Graph\Beta\Generated\Models\RecurrenceRangeType;
use Microsoft\Kiota\Abstractions\Types\Date;
use Microsoft\Graph\Beta\Generated\Models\Location;
use Microsoft\Graph\Beta\Generated\Models\Attendee;
use Microsoft\Graph\Beta\Generated\Models\EmailAddress;
use Microsoft\Graph\Beta\Generated\Models\AttendeeType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Event();
$requestBody->setSubject('Let\'s go for lunch');
$body = new ItemBody();
$body->setContentType(new BodyType('hTML'));
$body->setContent('Does noon time work for you?');
$requestBody->setBody($body);
$start = new DateTimeTimeZone();
$start->setDateTime('2017-09-04T12:00:00');
$start->setTimeZone('Pacific Standard Time');
$requestBody->setStart($start);
$end = new DateTimeTimeZone();
$end->setDateTime('2017-09-04T14:00:00');
$end->setTimeZone('Pacific Standard Time');
$requestBody->setEnd($end);
$recurrence = new PatternedRecurrence();
$recurrencePattern = new RecurrencePattern();
$recurrencePattern->setType(new RecurrencePatternType('weekly'));
$recurrencePattern->setInterval(1);
$recurrencePattern->setDaysOfWeek([new DayOfWeek('monday'),	]);
$recurrence->setPattern($recurrencePattern);
$recurrenceRange = new RecurrenceRange();
$recurrenceRange->setType(new RecurrenceRangeType('endDate'));
$recurrenceRange->setStartDate(new Date('2017-09-04'));
$recurrenceRange->setEndDate(new Date('2017-12-31'));
$recurrence->setRange($recurrenceRange);
$requestBody->setRecurrence($recurrence);
$location = new Location();
$location->setDisplayName('Harry\'s Bar');
$requestBody->setLocation($location);
$attendeesAttendee1 = new Attendee();
$attendeesAttendee1EmailAddress = new EmailAddress();
$attendeesAttendee1EmailAddress->setAddress('AdeleV@contoso.com');
$attendeesAttendee1EmailAddress->setName('Adele Vance');
$attendeesAttendee1->setEmailAddress($attendeesAttendee1EmailAddress);
$attendeesAttendee1->setType(new AttendeeType('required'));
$attendeesArray []= $attendeesAttendee1;
$requestBody->setAttendees($attendeesArray);


$result = $graphServiceClient->me()->events()->post($requestBody)->wait();

```