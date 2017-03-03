---
title: /verify
position: 1.3
type: post
description: Verify the U2F sign return URL
right_code: |
  ~~~ json
  {
      "code": 200,
      "message": "The URL was valid"
  }
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "code": 401,
    "message": "Session expired"
  }

  {
    "code": 401,
    "message": "Signature invalid"
  }

  {
    "code": 404,
    "message": "Return URL not found"
  }
  ~~~
  {: title="Error" }
---
username
: The username that tries to login to your application

returnUrl
: The return URL after successful authenticated a U2F Security Key

challenge
: The random challenge that generated in our BAO server

signature
: The signature that signed with your API KEY and its SECRET.

After the user successful authenticated with our FIDO server, is will jump back
to the return URL that generated with the API:

```
POST /signURL
```

Your application should verify the U2F sign return URL with this API that making
sure the U2F authentication was genuine.

This also prevent MitM and phishing attacks to your application.
{: .success }

Very important that your application calling this API in order to finish the whole authentication process.
{: .info }
