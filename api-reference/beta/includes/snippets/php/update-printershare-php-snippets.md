---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\PrinterShare;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new PrinterShare();
$requestBody->setDisplayName('ShareName');
$requestBody->setAllowAllUsers(true);
$additionalData = [
	'printer@odata.bind' => 'https://graph.microsoft.com/beta/print/printers/{id}',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->escapedPrint()->shares()->byPrinterShareId('printerShare-id')->patch($requestBody)->wait();

```