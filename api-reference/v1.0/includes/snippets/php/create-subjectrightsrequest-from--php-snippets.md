---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\SubjectRightsRequest;
use Microsoft\Graph\Generated\Models\SubjectRightsRequestType;
use Microsoft\Graph\Generated\Models\DataSubjectType;
use Microsoft\Graph\Generated\Models\DataSubject;
use Microsoft\Graph\Generated\Models\SubjectRightsRequestAllSiteLocation;
use Microsoft\Graph\Generated\Models\User;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SubjectRightsRequest();
$requestBody->setType(new SubjectRightsRequestType('export'));
$requestBody->setContentQuery('((\"Diego Siciliani\" OR \"Diego.Siciliani@contoso.com\") OR (participants:\"Diego.Siciliani@contoso.com\"))');
$requestBody->setDataSubjectType(new DataSubjectType('customer'));
$requestBody->setExternalId('F53BF2DA-607D-412A-B568-FAA0F023AC0B');
$requestBody->setDisplayName('Export report for customer Id: 12345');
$requestBody->setDescription('This is a export request');
$requestBody->setIncludeAllVersions(false);
$requestBody->setIncludeAuthoredContent(true);
$requestBody->setInternalDueDateTime(new \DateTime('2022-07-20T22:42:28Z'));
$dataSubject = new DataSubject();
$dataSubject->setFirstName('Diego');
$dataSubject->setLastName('Siciliani');
$dataSubject->setEmail('Diego.Siciliani@contoso.com');
$dataSubject->setResidency('USA');
$requestBody->setDataSubject($dataSubject);
$requestBody->setMailboxLocations(null);
$requestBody->setPauseAfterEstimate(true);
$requestBody->setRegulations(['CCPA', 	]);
$siteLocations = new SubjectRightsRequestAllSiteLocation();
$siteLocations->setOdataType('microsoft.graph.subjectRightsRequestAllSiteLocation');
$requestBody->setSiteLocations($siteLocations);
$approversUser1 = new User();
$approversUser1->setId('1B761ED2-AA7E-4D82-9CF5-C09D737B6167');
$approversArray []= $approversUser1;
$requestBody->setApprovers($approversArray);


$result = $graphServiceClient->privacy()->subjectRightsRequests()->post($requestBody)->wait();

```