---
title: /regRequest
position: 1.1
type: post
description: Return an array of UAF registration requests.
right_code: |
  ~~~ json
  {
      "code": 200,
      "message": [
          {
              "header": {
                  "upv": {
                      "major": 1,
                      "minor": 0
                  },
                  "op": "Reg",
                  "appID": "https://api.baosec.com/fido/facets",
                  "serverData": "VHd2QXpTYTBUMkI5TndpWUVDazlUdjAwRmEyMDVEWTNVbVh5RnpaV0FLay5NVFE1TVRNd016Z3lOVFkxTmcuWVhOay5Ta1JLYUVwRVJYZEtSVEZhVm10M2RscEViRXRqYlZwellUQndRbFpIYkd0V1YwWkhUbFU0",
                  "exts": null
              },
              "challenge": "JDJhJDEwJE1ZVkwvZDlKcmZsa0pBVGlkVWFGNU8",
              "username": "bao",
              "policy": {
                  "accepted": [
                      [
                          {
                              "aaid": [
                                  "BATS#0001"
                              ],
                              "vendorID": null,
                              "keyIDs": null,
                              "userVerification": 0,
                              "keyProtection": 0,
                              "matcherProtection": 0,
                              "attachmentHint": 0,
                              "tcDisplay": 0,
                              "authenticationAlgorithms": null,
                              "assertionSchemes": null,
                              "attestationTypes": null,
                              "authenticatorVersion": 0,
                              "exts": null
                          }
                      ],
                      [
                          {
                              "aaid": [
                                  "ABCD#ABCD"
                              ],
                              "vendorID": null,
                              "keyIDs": null,
                              "userVerification": 0,
                              "keyProtection": 0,
                              "matcherProtection": 0,
                              "attachmentHint": 0,
                              "tcDisplay": 0,
                              "authenticationAlgorithms": null,
                              "assertionSchemes": null,
                              "attestationTypes": null,
                              "authenticatorVersion": 0,
                              "exts": null
                          }
                      ],
                      [
                          {
                              "aaid": [
                                  "EBA0#0001"
                              ],
                              "vendorID": null,
                              "keyIDs": null,
                              "userVerification": 0,
                              "keyProtection": 0,
                              "matcherProtection": 0,
                              "attachmentHint": 0,
                              "tcDisplay": 0,
                              "authenticationAlgorithms": null,
                              "assertionSchemes": null,
                              "attestationTypes": null,
                              "authenticatorVersion": 0,
                              "exts": null
                          }
                      ]
                  ],
                  "disallowed": null
              }
          }
      ]
  }
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "code": 400,
    "message": "Unknown username <username>"
  }
  ~~~
  {: title="Error" }
---

username
: The username

Return an [UAF registration requests](https://fidoalliance.org/specs/fido-uaf-v1.1-id-20170202/fido-uaf-protocol-v1.1-id-20170202.html#registrationrequest-dictionary) array with the given username.

Each UAF registration request contains the UAF version that server supports.
{: .success }

The username must be unique in your application such as an email address.
{: .info }
