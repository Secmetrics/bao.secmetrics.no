---
title: /greeting
position: 1.0
type: get
description: Greeting with our UAF API for testing your API KEY
right_code: |
  ~~~ json
  {
    "code": 200,
    "message": "Hello BAO UAF"
  }
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "code": 401,
    "message": "API KEY invalid"
  }
  ~~~
  {: title="Error" }
---

Say hallo to our UAF API :-)
