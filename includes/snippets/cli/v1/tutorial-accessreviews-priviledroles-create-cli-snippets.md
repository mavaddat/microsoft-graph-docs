---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash


mgc identity-governance access-reviews definitions create --body '{\
    "displayName": "Review access of users and groups to privileged roles",\
    "descriptionForAdmins": "Review access of users and groups to privileged roles",\
    "scope": {\
        "@odata.type": "#microsoft.graph.principalResourceMembershipsScope",\
        "principalScopes": [\
            {\
                "@odata.type": "#microsoft.graph.accessReviewQueryScope",\
                "query": "/users",\
                "queryType": "MicrosoftGraph"\
            },\
            {\
                "@odata.type": "#microsoft.graph.accessReviewQueryScope",\
                "query": "/groups",\
                "queryType": "MicrosoftGraph"\
            }\
        ],\
        "resourceScopes": [\
            {\
                "@odata.type": "#microsoft.graph.accessReviewQueryScope",\
                "query": "/roleManagement/directory/roleDefinitions/fe930be7-5e62-47db-91af-98c3a49a38b1",\
                "queryType": "MicrosoftGraph"\
            }\
        ]\
    },\
    "reviewers": [\
        {\
            "query": "/users/2560f739-2e0e-4550-9fa0-1a1e67ae0ab8",\
            "queryType": "MicrosoftGraph"\
        }\
    ],\
    "settings": {\
        "mailNotificationsEnabled": true,\
        "reminderNotificationsEnabled": true,\
        "justificationRequiredOnApproval": true,\
        "defaultDecisionEnabled": false,\
        "defaultDecision": "None",\
        "instanceDurationInDays": 1,\
        "recommendationsEnabled": false,\
        "recurrence": {\
            "pattern": {\
                "type": "absoluteMonthly",\
                "interval": 3\
            },\
            "range": {\
                "type": "noEnd",\
                "startDate": "2024-03-25"\
            }\
        }\
    }\
}\
'

```