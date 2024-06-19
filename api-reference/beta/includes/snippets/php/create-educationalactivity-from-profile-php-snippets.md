---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\EducationalActivity;
use Microsoft\Kiota\Abstractions\Types\Date;
use Microsoft\Graph\Beta\Generated\Models\InstitutionData;
use Microsoft\Graph\Beta\Generated\Models\PhysicalAddress;
use Microsoft\Graph\Beta\Generated\Models\PhysicalAddressType;
use Microsoft\Graph\Beta\Generated\Models\EducationalActivityDetail;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new EducationalActivity();
$requestBody->setCompletionMonthYear(new Date('Date'));
$requestBody->setEndMonthYear(new Date('Date'));
$institution = new InstitutionData();
$institution->setDescription(null);
$institution->setDisplayName('Colorado State University');
$institutionLocation = new PhysicalAddress();
$institutionLocation->setType(new PhysicalAddressType('business'));
$institutionLocation->setPostOfficeBox(null);
$institutionLocation->setStreet('12000 E Prospect Rd');
$institutionLocation->setCity('Fort Collins');
$institutionLocation->setState('Colorado');
$institutionLocation->setCountryOrRegion('USA');
$institutionLocation->setPostalCode('80525');
$institution->setLocation($institutionLocation);
$institution->setWebUrl('https://www.colostate.edu');
$requestBody->setInstitution($institution);
$program = new EducationalActivityDetail();
$program->setAbbreviation('MBA');
$program->setActivities(null);
$program->setAwards(null);
$program->setDescription('Master of Business Administration with a major in Entreprenuership and Finance.');
$program->setDisplayName('Master of Business Administration');
$program->setFieldsOfStudy(null);
$program->setGrade('3.9');
$program->setNotes(null);
$program->setWebUrl('https://biz.colostate.edu');
$requestBody->setProgram($program);
$requestBody->setStartMonthYear(new Date('Date'));

$result = $graphServiceClient->me()->profile()->educationalActivities()->post($requestBody)->wait();

```