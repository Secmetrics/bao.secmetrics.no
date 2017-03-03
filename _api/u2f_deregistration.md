---
title: u2f/v1/deregistration
position: 1.6
type: post
description: Deregister the U2F Security Key
right_code: |
  ~~~ json
  {
  "code": 200,
  "message": "The U2F Security Key deregistered"
  }
  ~~~
  {: title="Response" }

  ~~~ json
  {
  "code": 404,
  "message": "Unknown username or publicKey"
  }
  ~~~
  {: title="Error" }
---

username
: The username

publicKey
: The public key of this U2F Security Key

Deregister the U2F Security Key with the given username and public key. Those parameters
are obtained within the list by calling the API /u2f/v1/registrations

The username must be unique in your application such as an email address.
{: .info }
