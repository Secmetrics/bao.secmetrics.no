---
title: /registrations
position: 1.5
type: post
description: Return a list of registered U2F Security Keys.
right_code: |
  ~~~ json
  {
    "code": 200,
    "message": [
        {
          "username": "username@example.com",
          "version": "U2F_V2",
          "enrollmentTime": 1488384211452,
          "publicKey": "048875122a3bb2b78289461780fcba0a1b4bc0dbf2c7963597ed06c40ac0e6b2d4a146274efc8f4dd8ae547164ae2e2e8218567d592a75e23b530e8ae9eb993739",
          "vendor": "Yubico U2F EE Serial 1432534688"
        },
        {
          "username": "username@example.com",
          "version": "U2F_V2",
          "enrollmentTime": 1488400884950,
          "publicKey": "04916037c8e39ce849d6f52bc865fb20f05512ddc4fd6c31e08932a0704cfa50d6c307f432a61b87e28615ce62a1e5a2d5ab011653aea4c94fa508d52bf8b2bd76",
          "vendor": "U2F Security Key--05898144877948084932"
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

Return a list of registered U2F Security Keys with the given username. The list
will be empty if the user does not have any U2F Security Key registered.

Show the list in your username's profile so he can choose to deregister a certain U2F Security Key when wanted.
{: .success }

The username must be unique in your application such as an email address.
{: .info }
