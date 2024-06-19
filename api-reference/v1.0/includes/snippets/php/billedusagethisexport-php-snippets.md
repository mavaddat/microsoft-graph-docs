---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Reports\Partners\Billing\Usage\Billed\MicrosoftGraphPartnersBillingExport\ExportPostRequestBody;
use Microsoft\Graph\Generated\Models\Partners\Billing\AttributeSet;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ExportPostRequestBody();
$requestBody->setInvoiceId('G016907411');
$requestBody->setAttributeSet(new AttributeSet('full'));

$result = $graphServiceClient->reports()->partners()->billing()->usage()->billed()->microsoftGraphPartnersBillingExport()->post($requestBody)->wait();

```