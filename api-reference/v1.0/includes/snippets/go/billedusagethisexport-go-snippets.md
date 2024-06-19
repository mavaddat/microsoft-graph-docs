---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v1.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphreports "github.com/microsoftgraph/msgraph-sdk-go/reports"
	  graphmodelspartnersbilling "github.com/microsoftgraph/msgraph-sdk-go/models/partners/billing"
	  //other-imports
)

requestBody := graphreports.NewExportPostRequestBody()
invoiceId := "G016907411"
requestBody.SetInvoiceId(&invoiceId) 
attributeSet := graphmodels.FULL_ATTRIBUTESET 
requestBody.SetAttributeSet(&attributeSet) 

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
microsoftGraphPartnersBillingExport, err := graphClient.Reports().Partners().Billing().Usage().Billed().MicrosoftGraphPartnersBillingExport().Post(context.Background(), requestBody, nil)


```