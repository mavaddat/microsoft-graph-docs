---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\CrossTenantAccessPolicyConfigurationDefault;
use Microsoft\Graph\Generated\Models\DefaultInvitationRedemptionIdentityProviderConfiguration;
use Microsoft\Graph\Generated\Models\B2bIdentityProvidersType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CrossTenantAccessPolicyConfigurationDefault();
$invitationRedemptionIdentityProviderConfiguration = new DefaultInvitationRedemptionIdentityProviderConfiguration();
$invitationRedemptionIdentityProviderConfiguration->setPrimaryIdentityProviderPrecedenceOrder([new B2bIdentityProvidersType('externalFederation'),new B2bIdentityProvidersType('azureActiveDirectory'),new B2bIdentityProvidersType('socialIdentityProviders'),	]);
$invitationRedemptionIdentityProviderConfiguration->setFallbackIdentityProvider(new B2bIdentityProvidersType('emailOneTimePasscode'));
$requestBody->setInvitationRedemptionIdentityProviderConfiguration($invitationRedemptionIdentityProviderConfiguration);

$result = $graphServiceClient->policies()->crossTenantAccessPolicy()->escapedDefault()->patch($requestBody)->wait();

```