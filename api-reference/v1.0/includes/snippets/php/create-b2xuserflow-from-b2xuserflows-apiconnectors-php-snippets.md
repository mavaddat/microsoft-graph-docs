---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\B2xIdentityUserFlow;
use Microsoft\Graph\Generated\Models\UserFlowType;
use Microsoft\Graph\Generated\Models\UserFlowApiConnectorConfiguration;
use Microsoft\Graph\Generated\Models\IdentityApiConnector;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new B2xIdentityUserFlow();
$requestBody->setId('UserFlowWithAPIConnector');
$requestBody->setUserFlowType(new UserFlowType('signUpOrSignIn'));
$requestBody->setUserFlowTypeVersion(1);
$apiConnectorConfiguration = new UserFlowApiConnectorConfiguration();
$apiConnectorConfigurationPostFederationSignup = new IdentityApiConnector();
$additionalData = [
	'@odata.id' => 'https://graph.microsoft.com/v1/identity/apiConnectors/{id}',
];
$apiConnectorConfigurationPostFederationSignup->setAdditionalData($additionalData);
$apiConnectorConfiguration->setPostFederationSignup($apiConnectorConfigurationPostFederationSignup);
$apiConnectorConfigurationPostAttributeCollection = new IdentityApiConnector();
$additionalData = [
	'@odata.id' => 'https://graph.microsoft.com/v1/identity/apiConnectors/{id}',
];
$apiConnectorConfigurationPostAttributeCollection->setAdditionalData($additionalData);
$apiConnectorConfiguration->setPostAttributeCollection($apiConnectorConfigurationPostAttributeCollection);
$requestBody->setApiConnectorConfiguration($apiConnectorConfiguration);

$result = $graphServiceClient->identity()->b2xUserFlows()->post($requestBody)->wait();

```