---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v1.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodelsidentitygovernance "github.com/microsoftgraph/msgraph-sdk-go/models/identitygovernance"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

requestBody := graphmodelsidentitygovernance.NewWorkflow()
displayName := "Onboard pre-hire employee"
requestBody.SetDisplayName(&displayName) 
description := "Configure pre-hire tasks for onboarding employees before their first day"
requestBody.SetDescription(&description) 
isEnabled := true
requestBody.SetIsEnabled(&isEnabled) 
isSchedulingEnabled := false
requestBody.SetIsSchedulingEnabled(&isSchedulingEnabled) 
executionConditions := graphmodelsidentitygovernance.NewTriggerAndScopeBasedConditions()
scope := graphmodelsidentitygovernance.NewRuleBasedSubjectSet()
rule := "(department eq 'Sales')"
scope.SetRule(&rule) 
executionConditions.SetScope(scope)
trigger := graphmodelsidentitygovernance.NewTimeBasedAttributeTrigger()
timeBasedAttribute := graphmodels.EMPLOYEEHIREDATE_WORKFLOWTRIGGERTIMEBASEDATTRIBUTE 
trigger.SetTimeBasedAttribute(&timeBasedAttribute) 
offsetInDays := int32(-2)
trigger.SetOffsetInDays(&offsetInDays) 
executionConditions.SetTrigger(trigger)
requestBody.SetExecutionConditions(executionConditions)


task := graphmodelsidentitygovernance.NewTask()
isEnabled := true
task.SetIsEnabled(&isEnabled) 
category := graphmodels.JOINER_LIFECYCLETASKCATEGORY 
task.SetCategory(&category) 
taskDefinitionId := "1b555e50-7f65-41d5-b514-5894a026d10d"
task.SetTaskDefinitionId(&taskDefinitionId) 
displayName := "Generate TAP And Send Email"
task.SetDisplayName(&displayName) 
description := "Generate Temporary Access Pass and send via email to user's manager"
task.SetDescription(&description) 


keyValuePair := graphmodels.NewKeyValuePair()
name := "tapLifetimeMinutes"
keyValuePair.SetName(&name) 
value := "480"
keyValuePair.SetValue(&value) 
keyValuePair1 := graphmodels.NewKeyValuePair()
name := "tapIsUsableOnce"
keyValuePair1.SetName(&name) 
value := "true"
keyValuePair1.SetValue(&value) 

arguments := []graphmodels.KeyValuePairable {
	keyValuePair,
	keyValuePair1,
}
task.SetArguments(arguments)

tasks := []graphmodelsidentitygovernance.Taskable {
	task,
}
requestBody.SetTasks(tasks)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
workflows, err := graphClient.IdentityGovernance().LifecycleWorkflows().Workflows().Post(context.Background(), requestBody, nil)


```