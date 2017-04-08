---
title: /deregRequest
position: 1.5
type: post
description: De-register UAF authentication(s)
right_code: |
  ~~~ json
  {
    "code": 200,
    "message": "Authentication(s) de-registered"
  }
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "code": 400,
    "message": "Failure: problem processing deregistration request"
  }
  ~~~
  {: title="Error" }
---

deregRequest
: The array of [UAF Deregistration Request](https://fidoalliance.org/specs/fido-uaf-v1.1-id-20170202/fido-uaf-protocol-v1.1-id-20170202.html#deregistration-request-message)

De-register UAF authentication(s) on the server and device.

Each UAF deregistration request contains the UAF version that server supports.
{: .success }

"deregRequest" is a serialized JSON array
{: .info }
