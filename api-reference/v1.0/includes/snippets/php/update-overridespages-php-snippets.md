---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Identity\B2xUserFlows\Item\Languages\Item\OverridesPages\Item\Value\$valuePutRequestBody;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new $valuePutRequestBody();
$additionalData = [
	'LocalizedStrings' => [
			[
				'elementType' => 'UxElement',
				'elementId' => null,
				'stringId' => 'alert_message',
				'override' => true,
				'value' => 'Are you sure that you want to cancel entering your information?',
			],
		],
];
$requestBody->setAdditionalData($additionalData);

$graphServiceClient->identity()->b2xUserFlows()->byB2xIdentityUserFlowId('b2xIdentityUserFlow-id')->languages()->byUserFlowLanguageConfigurationId('userFlowLanguageConfiguration-id')->overridesPages()->byUserFlowLanguagePageId('userFlowLanguagePage-id')->content()->put($requestBody)->wait();

```