---
title: u2f/v1/hasRegisteredKeys
position: 1.4
type: post
description: Check if the user has one or more U2F Security Keys registered.
right_code: |
  ~~~ json
  {
  "code": 200,
  "message": "User <username@example.com> has registered key(s)"
  }
  ~~~
  {: title="Response" }

  ~~~ json
  {
  "code": 400,
  "message": "Unknown username <username>"
  }

  {
  "code": 404,
  "message": "User <username@example.com> does not have any registered key"
  }
  ~~~
  {: title="Error" }
---

username
: The username

Check if the user has one or more Security Keys registered. If so, your application
should jump to our FIDO server page URL by calling the API /u2f/v1/sdk/generateSignURL
In order to authenticate the user with the given username.

The username must be unique in your application such as an email address.
{: .info }