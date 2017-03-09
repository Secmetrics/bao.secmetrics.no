---
title: Introduction
position: 2
---

BAO - Better Authentication Online is a fully [FIDO](https://fidoalliance.org/)
(Fast Identity Online) compliant solution for [SMEs](https://en.wikipedia.org/wiki/Small_and_medium-sized_enterprises).
It provides strong authentication cloud services that can be easily integrated into SMEs'
existing systems in both server and client sides. In addition, developers do not need to
change the existing infrastructure like a database, just call our API and you are ready to go!

![BAO Component](/images/bao-components.png)
{: .img-responsive }

In order to use BAO, you need to create an application on our Web [Console](https://console.baosec.com),
then follow the API instruction to complete the integration.

The following example logic flow shows an U2F Registration process by using BAO:

1. Call /registerURL API to get a registration URL
2. Redirect you web application to this URL
3. User plug in an U2F Security Key like a baoKey, and touch it for the confirmation
4. Our BAO FIDO server will verify the U2F Security Key, and redirect to the "returnUrl" you provided if succeed, otherwise back to the last page.
5. The user now registered a new U2F Security Key

The following example logic flow shows an U2F Authentication process by using BAO:

1. Call /signURL API to get an authentication URL
2. Redirect you web application to this URL
3. User plug in an U2F Security Key like a baoKey, and touch it for the confirmation
4. Our BAO FIDO server will verify the U2F Security Key, and redirect to the "returnUrl" you provided if succeed, otherwise back to the last page.
5. Call /verify API to verify the "returnUrl" with parameters that redirected to your web application which is important to prevent MitM and phishing attacks
6. Let your user login if succeed, otherwise back to the login page.
