---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\User;
use Microsoft\Graph\Beta\Generated\Models\ObjectIdentity;
use Microsoft\Graph\Beta\Generated\Models\PasswordProfile;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new User();
$requestBody->setDisplayName('John Smith');
$identitiesObjectIdentity1 = new ObjectIdentity();
$identitiesObjectIdentity1->setSignInType('userName');
$identitiesObjectIdentity1->setIssuer('contoso.com');
$identitiesObjectIdentity1->setIssuerAssignedId('johnsmith');
$identitiesArray []= $identitiesObjectIdentity1;
$identitiesObjectIdentity2 = new ObjectIdentity();
$identitiesObjectIdentity2->setSignInType('emailAddress');
$identitiesObjectIdentity2->setIssuer('contoso.com');
$identitiesObjectIdentity2->setIssuerAssignedId('jsmith@yahoo.com');
$identitiesArray []= $identitiesObjectIdentity2;
$identitiesObjectIdentity3 = new ObjectIdentity();
$identitiesObjectIdentity3->setSignInType('federated');
$identitiesObjectIdentity3->setIssuer('facebook.com');
$identitiesObjectIdentity3->setIssuerAssignedId('5eecb0cd');
$identitiesArray []= $identitiesObjectIdentity3;
$requestBody->setIdentities($identitiesArray);

$passwordProfile = new PasswordProfile();
$passwordProfile->setPassword('password-value');
$passwordProfile->setForceChangePasswordNextSignIn(false);
$requestBody->setPasswordProfile($passwordProfile);
$requestBody->setPasswordPolicies('DisablePasswordExpiration');

$result = $graphServiceClient->users()->post($requestBody)->wait();

```