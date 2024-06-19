---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphusers "github.com/microsoftgraph/msgraph-beta-sdk-go/users"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

requestBody := graphusers.NewItemSendMailPostRequestBody()
message := graphmodels.NewMessage()
subject := "Meet for lunch?"
message.SetSubject(&subject) 
body := graphmodels.NewItemBody()
contentType := graphmodels.TEXT_BODYTYPE 
body.SetContentType(&contentType) 
content := "The new cafeteria is open."
body.SetContent(&content) 
message.SetBody(body)


recipient := graphmodels.NewRecipient()
emailAddress := graphmodels.NewEmailAddress()
address := "meganb@contoso.com"
emailAddress.SetAddress(&address) 
recipient.SetEmailAddress(emailAddress)

toRecipients := []graphmodels.Recipientable {
	recipient,
}
message.SetToRecipients(toRecipients)


attachment := graphmodels.NewFileAttachment()
name := "attachment.txt"
attachment.SetName(&name) 
contentType := "text/plain"
attachment.SetContentType(&contentType) 
contentBytes := []byte("sGVsbG8gV29ybGQh")
attachment.SetContentBytes(&contentBytes) 

attachments := []graphmodels.Attachmentable {
	attachment,
}
message.SetAttachments(attachments)
requestBody.SetMessage(message)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
graphClient.Me().SendMail().Post(context.Background(), requestBody, nil)


```