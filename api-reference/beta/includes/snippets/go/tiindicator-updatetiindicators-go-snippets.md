---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphsecurity "github.com/microsoftgraph/msgraph-beta-sdk-go/security"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

requestBody := graphsecurity.NewUpdateTiIndicatorsPostRequestBody()


tiIndicator := graphmodels.NewTiIndicator()
id := "c6fb948b-89c5-3bba-a2cd-a9d9a1e430e4"
tiIndicator.SetId(&id) 
additionalInformation := "mytest"
tiIndicator.SetAdditionalInformation(&additionalInformation) 
tiIndicator1 := graphmodels.NewTiIndicator()
id := "e58c072b-c9bb-a5c4-34ce-eb69af44fb1e"
tiIndicator1.SetId(&id) 
additionalInformation := "test again"
tiIndicator1.SetAdditionalInformation(&additionalInformation) 

value := []graphmodels.TiIndicatorable {
	tiIndicator,
	tiIndicator1,
}
requestBody.SetValue(value)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
updateTiIndicators, err := graphClient.Security().TiIndicators().UpdateTiIndicators().PostAsUpdateTiIndicatorsPostResponse(context.Background(), requestBody, nil)


```