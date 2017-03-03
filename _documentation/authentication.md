---
title: Authentication
position: 4
right_code: |
  ~~~ json
  "Authorization": "fido-auth API_KEY"
  ~~~
  {: title="Authentication" }
---

You need to be authenticated for all API requests. You can generate an API key
in our [BAO console](https://console.baosec.com).

Add the API key to all requests as an "Authorization" header.

Nothing will work unless you include this API key
{: .error }

NOTE: There is a space between "fido-auth" and "API_KEY", for example:
{: .info }

~~~ json
{
"Authorization": "fido-auth 6d4fa5eb-083f-4e1e-a944-37fa7cef1123"
}
~~~
