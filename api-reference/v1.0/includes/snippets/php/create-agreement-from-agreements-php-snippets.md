---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Agreement;
use Microsoft\Graph\Generated\Models\AgreementFileLocalization;
use Microsoft\Graph\Generated\Models\AgreementFileData;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Agreement();
$requestBody->setDisplayName('Contoso ToU for guest users');
$requestBody->setIsViewingBeforeAcceptanceRequired(true);
$filesAgreementFileLocalization1 = new AgreementFileLocalization();
$filesAgreementFileLocalization1->setFileName('TOU.pdf');
$filesAgreementFileLocalization1->setLanguage('en');
$filesAgreementFileLocalization1->setIsDefault(true);
$filesAgreementFileLocalization1FileData = new AgreementFileData();
$filesAgreementFileLocalization1FileData->setData(\GuzzleHttp\Psr7\Utils::streamFor(base64_decode('SGVsbG8gd29ybGQ=//truncated-binary')));
$filesAgreementFileLocalization1->setFileData($filesAgreementFileLocalization1FileData);
$filesArray []= $filesAgreementFileLocalization1;
$requestBody->setFiles($filesArray);


$result = $graphServiceClient->identityGovernance()->termsOfUse()->agreements()->post($requestBody)->wait();

```