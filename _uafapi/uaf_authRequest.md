---
title: /authRequest
position: 1.3
type: post
description: Return an array of UAF authentication requests.
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
                "op": "Auth",
                "appID": "https://api.baosec.com/fido/facets",
                "serverData": "NFhoU2l1X1JYX1h3Vm5SbU5ES2JOaF9Qc0I3WXl3a1ZwNHd0a0I1U3F2Yy5NVFE1TVRNd016a3hNelF3TUEuU2tSS2FFcEVSWGRLUjNkNFRqSndXRTFFUmxwVlNIQjBZVmN3TWxWWVpGaFNTRVYyWVZNMA",
                "exts": null
            },
            "challenge": "JDJhJDEwJGwxN2pXMDFZUHptaW02UXdXRHEvaS4",
            "transaction": null,
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
    "message": "Unknown error"
  }
  ~~~
  {: title="Error" }
---

trxContent
: OPTIONAL, [Transaction Content](https://fidoalliance.org/specs/fido-uaf-v1.1-id-20170202/fido-uaf-protocol-v1.1-id-20170202.html#widl-Transaction-content), must be not null or empty if present, must less than 200 characters.

trxType
: OPTIONAL, [Transaction Type](https://fidoalliance.org/specs/fido-uaf-v1.1-id-20170202/fido-uaf-protocol-v1.1-id-20170202.html#widl-Transaction-contentType) must be 'text/plain' if present.

Return an [UAF authentication requests](https://fidoalliance.org/specs/fido-uaf-v1.1-id-20170202/fido-uaf-protocol-v1.1-id-20170202.html#authenticationrequest-dictionary) array.

Each UAF authentication request contains the UAF version that server supports.
{: .success }

No parameters
{: .info }
