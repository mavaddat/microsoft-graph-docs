---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Print\Printers\Create\CreatePostRequestBody;
use Microsoft\Graph\Generated\Models\PrintCertificateSigningRequest;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CreatePostRequestBody();
$requestBody->setDisplayName('Test Printer');
$requestBody->setManufacturer('Test Printer Manufacturer');
$requestBody->setModel('Test Printer Model');
$requestBody->setPhysicalDeviceId(null);
$requestBody->setHasPhysicalDevice(false);
$certificateSigningRequest = new PrintCertificateSigningRequest();
$certificateSigningRequest->setContent('{content}');
$certificateSigningRequest->setTransportKey('{sampleTransportKey}');
$requestBody->setCertificateSigningRequest($certificateSigningRequest);
$requestBody->setConnectorId(null);

$graphServiceClient->escapedPrint()->printers()->create()->post($requestBody)->wait();

```