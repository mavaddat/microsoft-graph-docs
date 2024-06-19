---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Call;
use Microsoft\Graph\Generated\Models\Modality;
use Microsoft\Graph\Generated\Models\ServiceHostedMediaConfig;
use Microsoft\Graph\Generated\Models\MediaInfo;
use Microsoft\Graph\Generated\Models\ChatInfo;
use Microsoft\Graph\Generated\Models\OrganizerMeetingInfo;
use Microsoft\Graph\Generated\Models\IdentitySet;
use Microsoft\Graph\Generated\Models\Identity;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Call();
$requestBody->setOdataType('#microsoft.graph.call');
$requestBody->setCallbackUri('https://bot.contoso.com/callback');
$requestBody->setRequestedModalities([new Modality('audio'),	]);
$mediaConfig = new ServiceHostedMediaConfig();
$mediaConfig->setOdataType('#microsoft.graph.serviceHostedMediaConfig');
$preFetchMediaMediaInfo1 = new MediaInfo();
$preFetchMediaMediaInfo1->setUri('https://cdn.contoso.com/beep.wav');
$preFetchMediaMediaInfo1->setResourceId('f8971b04-b53e-418c-9222-c82ce681a582');
$preFetchMediaArray []= $preFetchMediaMediaInfo1;
$preFetchMediaMediaInfo2 = new MediaInfo();
$preFetchMediaMediaInfo2->setUri('https://cdn.contoso.com/cool.wav');
$preFetchMediaMediaInfo2->setResourceId('86dc814b-c172-4428-9112-60f8ecae1edb');
$preFetchMediaArray []= $preFetchMediaMediaInfo2;
$mediaConfig->setPreFetchMedia($preFetchMediaArray);

$requestBody->setMediaConfig($mediaConfig);
$chatInfo = new ChatInfo();
$chatInfo->setOdataType('#microsoft.graph.chatInfo');
$chatInfo->setThreadId('19:meeting_Win6Ydo4wsMijFjZS00ZGVjLTk5MGUtOTRjNWY2NmNkYTFm@thread.v2');
$chatInfo->setMessageId('0');
$requestBody->setChatInfo($chatInfo);
$meetingInfo = new OrganizerMeetingInfo();
$meetingInfo->setOdataType('#microsoft.graph.organizerMeetingInfo');
$meetingInfoOrganizer = new IdentitySet();
$meetingInfoOrganizer->setOdataType('#microsoft.graph.identitySet');
$meetingInfoOrganizerUser = new Identity();
$meetingInfoOrganizerUser->setOdataType('#microsoft.graph.identity');
$meetingInfoOrganizerUser->setId('5810cede-f3cc-42eb-b2c1-e9bd5d53ec96');
$meetingInfoOrganizerUser->setDisplayName('Bob');
$additionalData = [
'tenantId' => '86dc81db-c112-4228-9222-63f3esaa1edb',
];
$meetingInfoOrganizerUser->setAdditionalData($additionalData);
$meetingInfoOrganizer->setUser($meetingInfoOrganizerUser);
$meetingInfo->setOrganizer($meetingInfoOrganizer);
$additionalData = [
'allowConversationWithoutHost' => true,
];
$meetingInfo->setAdditionalData($additionalData);
$requestBody->setMeetingInfo($meetingInfo);
$requestBody->setTenantId('86dc81db-c112-4228-9222-63f3esaa1edb');

$result = $graphServiceClient->communications()->calls()->post($requestBody)->wait();

```