---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

// Code snippets are only available for the latest version. Current version is 6.x

GraphServiceClient graphClient = new GraphServiceClient(requestAdapter);

Invitation invitation = new Invitation();
invitation.setInvitedUserEmailAddress("admin@fabrikam.com");
invitation.setInviteRedirectUrl("https://myapp.contoso.com");
Invitation result = graphClient.invitations().post(invitation);


```