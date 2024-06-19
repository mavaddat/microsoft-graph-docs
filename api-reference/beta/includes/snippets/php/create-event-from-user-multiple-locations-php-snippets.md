---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Users\Item\Events\EventsRequestBuilderPostRequestConfiguration;
use Microsoft\Graph\Beta\Generated\Models\Event;
use Microsoft\Graph\Beta\Generated\Models\ItemBody;
use Microsoft\Graph\Beta\Generated\Models\BodyType;
use Microsoft\Graph\Beta\Generated\Models\DateTimeTimeZone;
use Microsoft\Graph\Beta\Generated\Models\Attendee;
use Microsoft\Graph\Beta\Generated\Models\EmailAddress;
use Microsoft\Graph\Beta\Generated\Models\AttendeeType;
use Microsoft\Graph\Beta\Generated\Models\Location;
use Microsoft\Graph\Beta\Generated\Models\LocationType;
use Microsoft\Graph\Beta\Generated\Models\PhysicalAddress;
use Microsoft\Graph\Beta\Generated\Models\OutlookGeoCoordinates;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Event();
$requestBody->setSubject('Plan summer company picnic');
$body = new ItemBody();
$body->setContentType(new BodyType('hTML'));
$body->setContent('Let\'s kick-start this event planning!');
$requestBody->setBody($body);
$start = new DateTimeTimeZone();
$start->setDateTime('2017-08-30T11:00:00');
$start->setTimeZone('Pacific Standard Time');
$requestBody->setStart($start);
$end = new DateTimeTimeZone();
$end->setDateTime('2017-08-30T12:00:00');
$end->setTimeZone('Pacific Standard Time');
$requestBody->setEnd($end);
$attendeesAttendee1 = new Attendee();
$attendeesAttendee1EmailAddress = new EmailAddress();
$attendeesAttendee1EmailAddress->setAddress('DanaS@contoso.com');
$attendeesAttendee1EmailAddress->setName('Dana Swope');
$attendeesAttendee1->setEmailAddress($attendeesAttendee1EmailAddress);
$attendeesAttendee1->setType(new AttendeeType('required'));
$attendeesArray []= $attendeesAttendee1;
$attendeesAttendee2 = new Attendee();
$attendeesAttendee2EmailAddress = new EmailAddress();
$attendeesAttendee2EmailAddress->setAddress('AlexW@contoso.com');
$attendeesAttendee2EmailAddress->setName('Alex Wilber');
$attendeesAttendee2->setEmailAddress($attendeesAttendee2EmailAddress);
$attendeesAttendee2->setType(new AttendeeType('required'));
$attendeesArray []= $attendeesAttendee2;
$requestBody->setAttendees($attendeesArray);

$location = new Location();
$location->setDisplayName('Conf Room 3; Fourth Coffee; Home Office');
$location->setLocationType(new LocationType('default'));
$requestBody->setLocation($location);
$locationsLocation1 = new Location();
$locationsLocation1->setDisplayName('Conf Room 3');
$locationsArray []= $locationsLocation1;
$locationsLocation2 = new Location();
$locationsLocation2->setDisplayName('Fourth Coffee');
$locationsLocation2Address = new PhysicalAddress();
$locationsLocation2Address->setStreet('4567 Main St');
$locationsLocation2Address->setCity('Redmond');
$locationsLocation2Address->setState('WA');
$locationsLocation2Address->setCountryOrRegion('US');
$locationsLocation2Address->setPostalCode('32008');
$locationsLocation2->setAddress($locationsLocation2Address);
$locationsLocation2Coordinates = new OutlookGeoCoordinates();
$locationsLocation2Coordinates->setLatitude(47.672);
$locationsLocation2Coordinates->setLongitude(-102.103);
$locationsLocation2->setCoordinates($locationsLocation2Coordinates);
$locationsArray []= $locationsLocation2;
$locationsLocation3 = new Location();
$locationsLocation3->setDisplayName('Home Office');
$locationsArray []= $locationsLocation3;
$requestBody->setLocations($locationsArray);

$requestBody->setAllowNewTimeProposals(true);
$requestConfiguration = new EventsRequestBuilderPostRequestConfiguration();
$headers = [
'Prefer' => 'outlook.timezone="Pacific Standard Time"',
];
$requestConfiguration->headers = $headers;


$result = $graphServiceClient->me()->events()->post($requestBody, $requestConfiguration)->wait();

```