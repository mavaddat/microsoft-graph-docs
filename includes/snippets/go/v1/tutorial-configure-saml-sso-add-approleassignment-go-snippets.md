---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v1.*

// Dependencies
import (
	  "context"
	  "github.com/google/uuid"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

requestBody := graphmodels.NewAppRoleAssignment()
principalId := uuid.MustParse("59bb3898-0621-4414-ac61-74f9d7201355")
requestBody.SetPrincipalId(&principalId) 
principalType := "User"
requestBody.SetPrincipalType(&principalType) 
appRoleId := uuid.MustParse("3a84e31e-bffa-470f-b9e6-754a61e4dc63")
requestBody.SetAppRoleId(&appRoleId) 
resourceId := uuid.MustParse("d3616293-fff8-4415-9f01-33b05dad1b46")
requestBody.SetResourceId(&resourceId) 

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
appRoleAssignments, err := graphClient.ServicePrincipals().ByServicePrincipalId("servicePrincipal-id").AppRoleAssignments().Post(context.Background(), requestBody, nil)


```