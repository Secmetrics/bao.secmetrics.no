---
title: POST Header
position: 5
right_code: |
  ```
    "Content-Type": "application/x-www-form-urlencoded"
  ```
  {: title="POST header" }
---

Your application will need to add a header in order to send a POST request.

Add "application/x-www-form-urlencoded" to all POST requests as a "Content-Type" header.
{: .success }

Nothing will work unless you include this header with the POST request.
{: .error }

~~~ json
  {
    "Content-Type": "application/x-www-form-urlencoded"
  }
~~~
