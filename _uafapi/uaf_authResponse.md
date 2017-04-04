---
title: /authResponse
position: 1.4
type: post
description: Process of UAF authentication responses sent from the client.
right_code: |
  ~~~ json
  {
    "code": 200,
    "message": [
        {
            "AAID": "BATS#0001",
            "KeyID": "SkRKaEpERXdKSFE1ZUc1Mlkxb3lkbmRTWjBkc1pHcEZXR2htTTA4",
            "deviceId": null,
            "username": "bao",
            "status": "SUCCESS"
        }
      ]
  }
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "code": 400,
    "message": "Unknown error"
  }
  ~~~
  {: title="Error" }
---

authResponse
: The array of [UAF Authentication Responses](https://fidoalliance.org/specs/fido-uaf-v1.1-id-20170202/fido-uaf-protocol-v1.1-id-20170202.html#authenticationresponse-dictionary)

Return the Authentication records that verified by server.

"authResponse" is a serialized JSON array
{: .info }
