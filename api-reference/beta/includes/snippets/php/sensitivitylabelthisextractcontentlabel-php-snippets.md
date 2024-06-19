---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Users\Item\Security\InformationProtection\SensitivityLabels\Microsoft\Graph\Security\ExtractContentLabel\ExtractContentLabelRequestBuilderPostRequestConfiguration;
use Microsoft\Graph\Beta\Generated\Users\Item\Security\InformationProtection\SensitivityLabels\MicrosoftGraphSecurityExtractContentLabel\ExtractContentLabelPostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\Security\ContentInfo;
use Microsoft\Graph\Beta\Generated\Models\Security\ContentState;
use Microsoft\Graph\Beta\Generated\Models\Security\KeyValuePair;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ExtractContentLabelPostRequestBody();
$contentInfo = new ContentInfo();
$contentInfo->setIdentifier('MyDoc.docx');
$contentInfo->setState(new ContentState('rest'));
$metadataKeyValuePair1 = new KeyValuePair();
$metadataKeyValuePair1->setName('MSIP_Label_0ed12617-d0ef-4053-b8e4-ecf5bcf2ffb3_Enabled');
$metadataKeyValuePair1->setValue('True');
$metadataArray []= $metadataKeyValuePair1;
$metadataKeyValuePair2 = new KeyValuePair();
$metadataKeyValuePair2->setName('MSIP_Label_0ed12617-d0ef-4053-b8e4-ecf5bcf2ffb3_Method');
$metadataKeyValuePair2->setValue('Standard');
$metadataArray []= $metadataKeyValuePair2;
$metadataKeyValuePair3 = new KeyValuePair();
$metadataKeyValuePair3->setName('MSIP_Label_0ed12617-d0ef-4053-b8e4-ecf5bcf2ffb3_SetDate');
$metadataKeyValuePair3->setValue('1/1/0001 12:00:00 AM');
$metadataArray []= $metadataKeyValuePair3;
$metadataKeyValuePair4 = new KeyValuePair();
$metadataKeyValuePair4->setName('MSIP_Label_0ed12617-d0ef-4053-b8e4-ecf5bcf2ffb3_SiteId');
$metadataKeyValuePair4->setValue('cfa4cf1d-a337-4481-aa99-19d8f3d63f7c');
$metadataArray []= $metadataKeyValuePair4;
$metadataKeyValuePair5 = new KeyValuePair();
$metadataKeyValuePair5->setName('MSIP_Label_0ed12617-d0ef-4053-b8e4-ecf5bcf2ffb3_Name');
$metadataKeyValuePair5->setValue('LabelScopedToBob_Tests');
$metadataArray []= $metadataKeyValuePair5;
$metadataKeyValuePair6 = new KeyValuePair();
$metadataKeyValuePair6->setName('MSIP_Label_0ed12617-d0ef-4053-b8e4-ecf5bcf2ffb3_ContentBits');
$metadataKeyValuePair6->setValue('0');
$metadataArray []= $metadataKeyValuePair6;
$metadataKeyValuePair7 = new KeyValuePair();
$metadataKeyValuePair7->setName('MSIP_Label_0ed12617-d0ef-4053-b8e4-ecf5bcf2ffb3_ActionId');
$metadataKeyValuePair7->setValue('00000000-0000-0000-0000-000000000000');
$metadataArray []= $metadataKeyValuePair7;
$contentInfo->setMetadata($metadataArray);

$additionalData = [
'format' => 'default',
];
$contentInfo->setAdditionalData($additionalData);
$requestBody->setContentInfo($contentInfo);
$requestConfiguration = new MicrosoftExtractContentLabelRequestBuilderPostRequestConfiguration();
$headers = [
	'User-Agent' => 'ContosoLOBApp/1.0',
];
$requestConfiguration->headers = $headers;


$result = $graphServiceClient->users()->byUserId('user-id')->security()->informationProtection()->sensitivityLabels()->microsoftGraphSecurityExtractContentLabel()->post($requestBody, $requestConfiguration)->wait();

```