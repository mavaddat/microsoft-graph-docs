---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodelsdevicemanagement "github.com/microsoftgraph/msgraph-beta-sdk-go/models/devicemanagement"
	  //other-imports
)

requestBody := graphmodelsdevicemanagement.NewAlertRule()
severity := graphmodels.INFORMATIONAL_RULESEVERITYTYPE 
requestBody.SetSeverity(&severity) 
enabled := true
requestBody.SetEnabled(&enabled) 
threshold := graphmodelsdevicemanagement.NewRuleThreshold()
aggregation := graphmodels.COUNT_AGGREGATIONTYPE 
threshold.SetAggregation(&aggregation) 
operator := graphmodels.GREATEROREQUAL_OPERATORTYPE 
threshold.SetOperator(&operator) 
target := int32(90)
threshold.SetTarget(&target) 
requestBody.SetThreshold(threshold)


ruleCondition := graphmodelsdevicemanagement.NewRuleCondition()
relationshipType := graphmodels.OR_RELATIONSHIPTYPE 
ruleCondition.SetRelationshipType(&relationshipType) 
conditionCategory := graphmodels.AZURENETWORKCONNECTIONCHECKFAILURES_CONDITIONCATEGORY 
ruleCondition.SetConditionCategory(&conditionCategory) 
aggregation := graphmodels.COUNT_AGGREGATIONTYPE 
ruleCondition.SetAggregation(&aggregation) 
operator := graphmodels.GREATEROREQUAL_OPERATORTYPE 
ruleCondition.SetOperator(&operator) 
thresholdValue := "90"
ruleCondition.SetThresholdValue(&thresholdValue) 

conditions := []graphmodelsdevicemanagement.RuleConditionable {
	ruleCondition,
}
requestBody.SetConditions(conditions)


notificationChannel := graphmodelsdevicemanagement.NewNotificationChannel()
notificationChannelType := graphmodels.PORTAL_NOTIFICATIONCHANNELTYPE 
notificationChannel.SetNotificationChannelType(&notificationChannelType) 
notificationReceivers := []graphmodelsdevicemanagement.NotificationReceiverable {

}
notificationChannel.SetNotificationReceivers(notificationReceivers)
notificationChannel1 := graphmodelsdevicemanagement.NewNotificationChannel()
notificationChannelType := graphmodels.EMAIL_NOTIFICATIONCHANNELTYPE 
notificationChannel1.SetNotificationChannelType(&notificationChannelType) 


notificationReceiver := graphmodelsdevicemanagement.NewNotificationReceiver()
locale := "en-us"
notificationReceiver.SetLocale(&locale) 
contactInformation := "serena.davis@contoso.com"
notificationReceiver.SetContactInformation(&contactInformation) 

notificationReceivers := []graphmodelsdevicemanagement.NotificationReceiverable {
	notificationReceiver,
}
notificationChannel1.SetNotificationReceivers(notificationReceivers)

notificationChannels := []graphmodelsdevicemanagement.NotificationChannelable {
	notificationChannel,
	notificationChannel1,
}
requestBody.SetNotificationChannels(notificationChannels)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
alertRules, err := graphClient.DeviceManagement().Monitoring().AlertRules().ByAlertRuleId("alertRule-id").Patch(context.Background(), requestBody, nil)


```