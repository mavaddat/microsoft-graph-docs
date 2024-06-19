---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const conversionUserDetails = {
    userPrincipalName: 'AdeleVance@contoso.com',
    passwordProfile: {
        password: 'Zdi087#2jhkahf',
        forceChangePasswordNextSignIn: 'true'
    },
    mail: 'AdeleV@contoso.com'
};

await client.api('/users/0b8cc234-ef87-4015-9785-cbb42000d41c/convertExternalToInternalMemberUser')
	.version('beta')
	.post(conversionUserDetails);

```