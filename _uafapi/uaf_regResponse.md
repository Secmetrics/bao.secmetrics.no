---
title: /regResponse
position: 1.2
type: post
description: Process of UAF registration responses sent from the client.
right_code: |
  ~~~ json
  {
    "code": 200,
    "message": [
        {
            "authenticator": {
                "AAID": "BATS#0001",
                "KeyID": "SkRKaEpERXdKSFE1ZUc1Mlkxb3lkbmRTWjBkc1pHcEZXR2htTTA4",
                "deviceId": null,
                "username": null,
                "status": null
            },
            "PublicKey": "BLilTYrPovMEzgXEFqYg_f8CAczMRcb9XHK28_-ao9UK818sFqL9HY5a_Z-FdIqIh1F8zxaNF1G6mjhVmUpP70k",
            "SignCounter": null,
            "AuthenticatorVersion": "0.0",
            "tcDisplayPNGCharacteristics": null,
            "username": "bao",
            "userId": null,
            "deviceId": null,
            "timeStamp": "1491303825656",
            "status": "SUCCESS",
            "attestCert": "MIICEjCCAbigAwIBAgIEWOIA0DAKBggqhkjOPQQDAjCBkDELMAkGA1UEBhMCTk8xEDAOBgNVBAgMB09QUExBTkQxDzANBgNVBAcMBkdKT1ZJSzEXMBUGA1UECgwOU2VjbWV0cmljcyBBUy4xDTALBgNVBAsMBEZJRE8xFjAUBgNVBAMMDVNlY21ldHJpY3MgQVMxHjAcBgkqhkiG9w0BCQEWD2ZpZG9AYmFvc2VjLmNvbTAeFw0xNzA0MDMwNzU5MTJaFw0yNzA0MDEwNzU5MTJaMIGQMQswCQYDVQQGEwJOTzEQMA4GA1UECAwHT1BQTEFORDEPMA0GA1UEBwwGR0pPVklLMRcwFQYDVQQKDA5TZWNtZXRyaWNzIEFTLjENMAsGA1UECwwERklETzEWMBQGA1UEAwwNU2VjbWV0cmljcyBBUzEeMBwGCSqGSIb3DQEJARYPZmlkb0BiYW9zZWMuY29tMFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAE5NS-0o_TFYZan2_g4fpSN1XPQDEaEWpXUJzOXkKW5YJ0tHtdIGKNVzEzw6T7MeEwrSk4OUE00SBNu74R242-tTAKBggqhkjOPQQDAgNIADBFAiAUNK7w4BKyvLnHp1EnSEFnBxxgcdUVfRDd9qID_7eP4wIhAL1vcosg55wWkm17IY0SGZiz3bJEECEHEHYxwpb66r9u",
            "attestDataToSign": "Az64AAsuCQBCQVRTIzAwMDEOLgcAAAABAQAAAQouIABarHj4cCmn03z6n1RxySL_i84TFJaoFw_xnlgent2BegkuJwBKREpoSkRFd0pIUTVlRzUyWTFveWRuZFNaMGRzWkdwRldHaG1NMDgNLggAAAABAAAAAQAMLkEABLilTYrPovMEzgXEFqYg_f8CAczMRcb9XHK28_-ao9UK818sFqL9HY5a_Z-FdIqIh1F8zxaNF1G6mjhVmUpP70k",
            "attestSignature": "eQPxzkLRkR2vs3NWKDvng-4WIrzfo6C9WV6bM8OrC-VscV4pPq1l4P4FIq7ke67odXnU2kAa39ZGYreEaDLM4A",
            "attestVerifiedStatus": "VALID"
        }
    ]
}
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "code": 409,
    "message": "Authenticator already Registered"
  }
  ~~~
  {: title="Error" }
---

regResponse
: The array of [UAF Registration Responses](https://fidoalliance.org/specs/fido-uaf-v1.1-id-20170202/fido-uaf-protocol-v1.1-id-20170202.html#registrationresponse-dictionary)

Return the Registration records that saved in the server side, only if the status was SUCCESS.

"regResponse" is a serialized JSON array
{: .info }
