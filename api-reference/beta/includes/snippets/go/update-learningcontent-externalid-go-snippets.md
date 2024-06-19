---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  "time"
	  abstractions "github.com/microsoft/kiota-abstractions-go"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

requestBody := graphmodels.NewLearningContent()
title := "Manage classes, resources, assessment, and planning in Microsoft Teams with Beedle"
requestBody.SetTitle(&title) 
description := "A module to guide users through the various teaching and learning enhancements that Beedle provides within Microsoft Teams, with many examples of everyday application."
requestBody.SetDescription(&description) 
contentWebUrl := "https://learn.microsoft.com/learn/modules/manage-classes-resources-assessment-planning-beedle/"
requestBody.SetContentWebUrl(&contentWebUrl) 
sourceName := "MsLearn"
requestBody.SetSourceName(&sourceName) 
thumbnailWebUrl := "https://syndetics.com/index.aspx?isbn=9783319672175/LC.GIF"
requestBody.SetThumbnailWebUrl(&thumbnailWebUrl) 
languageTag := "en-us"
requestBody.SetLanguageTag(&languageTag) 
numberOfPages := int32(9)
requestBody.SetNumberOfPages(&numberOfPages) 
duration , err := abstractions.ParseISODuration("PT20M")
requestBody.SetDuration(&duration) 
format := "Book"
requestBody.SetFormat(&format) 
level := graphmodels.BEGINNER_LEVEL 
requestBody.SetLevel(&level) 
createdDateTime , err := time.Parse(time.RFC3339, "2018-01-01T00:00:00")
requestBody.SetCreatedDateTime(&createdDateTime) 
lastModifiedDateTime , err := time.Parse(time.RFC3339, "2021-04-01T04:26:06.1995367Z")
requestBody.SetLastModifiedDateTime(&lastModifiedDateTime) 
additionalTags := []string {
	"Create private or public teams",
	"Add members to teams",
}
requestBody.SetAdditionalTags(additionalTags)
skillTags := []string {
	"Create teams",
	"Teams channels",
	"Teams members",
}
requestBody.SetSkillTags(skillTags)
isActive := true
requestBody.SetIsActive(&isActive) 
isPremium := false
requestBody.SetIsPremium(&isPremium) 
isSearchable := true
requestBody.SetIsSearchable(&isSearchable) 
additionalData := map[string]interface{}{
	"contributor" : "Scott Simpson", 
}
requestBody.SetAdditionalData(additionalData)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
externalId := "{externalId}"
learningContents, err := graphClient.EmployeeExperience().LearningProviders().ByLearningProviderId("learningProvider-id").LearningContentsWithExternalId(&externalId).Patch(context.Background(), requestBody, nil)


```