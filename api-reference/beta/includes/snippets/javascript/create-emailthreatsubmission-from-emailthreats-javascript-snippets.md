---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const emailThreatSubmission = {
  '@odata.type': '#microsoft.graph.security.emailUrlThreatSubmission',
  category: 'spam',
  recipientEmailAddress: 'tifc@contoso.com',
  messageUrl: 'https://graph.microsoft.com/beta/users/c52ce8db-3e4b-4181-93c4-7d6b6bffaf60/messages/AAMkADU3MWUxOTU0LWNlOTEt='
};

await client.api('/security/threatSubmission/emailThreats')
	.version('beta')
	.post(emailThreatSubmission);

```