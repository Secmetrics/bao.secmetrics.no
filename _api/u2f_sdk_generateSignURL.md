---
title: /u2f/v1/sdk/generateSignURL
position: 1.2
type: post
description: Generate an U2F sign URL
right_code: |
  ~~~ json
  {
      "code": 200,
      "message": "https://fido.baosec.com/api/u2f/v1/startAuthentication?username=example-user&returnUrl=https://example.com/u2fLogin&challenge=d39ea54d7a127294033f6d9ff43e5f3d1f6ded3194bc7cda70acb04d5601872c&signature=fb5dbff9c91d0c7f20b661e076f2a91fdf30512694ffbfef7c5fd056ad569739"
  }
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "code": 400,
    "message": "Bad URL format"
  }
  ~~~
  {: title="Error" }
---
username
: The username that tries to login to your application

returnUrl
: The return URL after successful authenticated a U2F Security Key

Generate an U2F sign URL with the given username and return URL and
redirecting to it with your application.

The username must be unique in your application such as an email address.
{: .info }

The full version of a sign return URL to your application will contain four Query Parameters, "username", "returnUrl", "challenge", and "signature". For example:
~~~ json
  https://example.com/u2flogin?username=xxx&returnUrl=xxx&challenge=xxx&signature=xxx
~~~
But when doing the request, just add for example "https://example.com/u2flogin" to the "returnUrl" parameter, we will generate the full version for your application. Making sure that you application has such an URL address in order to verify the sign return URL by calling /u2f/v1/sdk/verifySignReturnURL
{: .info }
