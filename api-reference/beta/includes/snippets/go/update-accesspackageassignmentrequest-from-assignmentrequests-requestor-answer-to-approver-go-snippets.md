---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

requestBody := graphmodels.NewAccessPackageAssignmentRequest()
id := "7a6ab703-0780-4b37-8445-81f679b2d75c"
requestBody.SetId(&id) 
requestType := "adminUpdate"
requestBody.SetRequestType(&requestType) 


accessPackageAnswer := graphmodels.NewAccessPackageAnswerString()
value := "UpdatedAnswerValue"
accessPackageAnswer.SetValue(&value) 
answeredQuestion := graphmodels.NewAccessPackageMultipleChoiceQuestion()
id := "8fe745e7-80b2-490d-bd22-4e708c77288c"
answeredQuestion.SetId(&id) 
accessPackageAnswer.SetAnsweredQuestion(answeredQuestion)
accessPackageAnswer1 := graphmodels.NewAccessPackageAnswerString()
value := "My updated answer."
accessPackageAnswer1.SetValue(&value) 
displayValue := "This is my updated answer to the question."
accessPackageAnswer1.SetDisplayValue(&displayValue) 
answeredQuestion := graphmodels.NewAccessPackageTextInputQuestion()
id := "7aaa18c9-8e4f-440f-bd5a-3a7ce312cbe6"
answeredQuestion.SetId(&id) 
accessPackageAnswer1.SetAnsweredQuestion(answeredQuestion)

answers := []graphmodels.AccessPackageAnswerable {
	accessPackageAnswer,
	accessPackageAnswer1,
}
requestBody.SetAnswers(answers)
additionalData := map[string]interface{}{
assignment := graph.New()
id := "44c741c1-2cf4-40db-83b6-e0112f8e5a83"
assignment.SetId(&id) 
	requestBody.SetAssignment(assignment)
}
requestBody.SetAdditionalData(additionalData)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
assignmentRequests, err := graphClient.IdentityGovernance().EntitlementManagement().AssignmentRequests().Post(context.Background(), requestBody, nil)


```