---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash


mgc-beta users send-mail post --user-id {user-id} --body '{\
  "message": {\
    "subject": "Meet for lunch?",\
    "body": {\
      "contentType": "Text",\
      "content": "The new cafeteria is open."\
    },\
    "toRecipients": [\
      {\
        "emailAddress": {\
          "address": "samanthab@contoso.com"\
        }\
      }\
    ],\
    "ccRecipients": [\
      {\
        "emailAddress": {\
          "address": "danas@contoso.com"\
        }\
      }\
    ]\
  },\
  "saveToSentItems": "false"\
}\
'

```