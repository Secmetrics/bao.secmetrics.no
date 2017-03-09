---
title: Introduction
position: 2
---

BAO - Better Authentication Online is a fully [FIDO](https://fidoalliance.org/)
(Fast Identity Online) compliant solution for [SMEs](https://en.wikipedia.org/wiki/Small_and_medium-sized_enterprises).
It provides strong and free authentication cloud services that can be easily integrated into SMEs'
existing systems in both server and client sides. In addition, developers do not need to
change the existing infrastructure like a database, just call our API and you are ready to go!

![BAO Component](/images/bao-components.png)
{: .img-responsive }

In order to use BAO, you need to create an application in our Web [Console](https://console.baosec.com),
then follow the API instruction to complete the integration.

##### The following example logic flow shows an U2F Registration process by using BAO: #####

1. Call /registerURL API to get a registration URL
2. Redirect you web application to this URL
3. User plug in an U2F Security Key like a baoKey, and touch it for the confirmation
4. Our BAO FIDO server will verify the U2F Security Key, and redirect to the "returnUrl" you provided if succeed, otherwise back to the last page.
5. The user now registered a new U2F Security Key

##### The following example logic flow shows an U2F Authentication process by using BAO: #####

1. Call /signURL API to get an authentication URL
2. Redirect you web application to this URL
3. User plug in an U2F Security Key like a baoKey, and touch it for the confirmation
4. Our BAO FIDO server will verify the U2F Security Key, and redirect to the "returnUrl" you provided if succeed, otherwise back to the last page.
5. Call /verify API to verify the "returnUrl" with parameters that redirected to your web application which is important to prevent MitM and phishing attacks
6. Let your user login if succeed, otherwise back to the login page.

#### Implementation Considerations ####

1. You can first try our [Console](https://console.baosec.com) to familiar with the process of our BAO FIDO authentication services by adding an U2F Security Key, like a baoKey or a Yubikey. Our BAO FIDO Server supports all U2F Security Keys on the market.
2. During the Registration, since your user has already logged in you web application, the "returnUrl" you can just put something like:
```
"https://yourwebapplication/profile"
```
3. While it's little bit complicate for the Authentication process, you have to make sure that the "returnUrl" that redirected to your web application was genuine. In this case, you need to have an URL path to consume those parameters like following, Please also refer to the /signURL API.
```
https://yourwebapplication/u2flogin?username=xxx&returnUrl=xxx&challenge=xxx&signature=xxx
```
4. It is important that you web application is fully covered by HTTPS, otherwise you web application is still vulnerable for MitM and phishing attacks.
5. DO NOT disclose your API KEY and its SECRET in any cases, and DO NOT use the API KEY to call our API in front-end JavaScript, make all the API calls in back-end.
6. Since FIDO standards are new to the web, only few browsers supported including Google Chrome version 38 or later, or Opera version 40 or later. Firefox is also supported however the add-on has to be installed [U2F Support Add-on](https://addons.mozilla.org/en-GB/firefox/addon/u2f-support-add-on/). Make sure that your users knowing this.
7. If you have any questions, please do not hesitate to send us an [email](mailto:beta@baosec.com), we will get back to you in 24 hours.
