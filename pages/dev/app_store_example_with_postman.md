# App Store Example using Postman

In this example, we'll use Postman to make an authorization request and
API call to the App Store.

*Postman is an Web API testing tool that runs on top of Google Chrome.
It can be downloaded for free and provides a practical example of an
external app interacting with the Industrial App Store. *

Download and install Postman to get started:
<https://www.getpostman.com>

#### App Store Authentication and API Call Example

In our example we'll prepare a request to the App Store API method:[GET
api/Resource/UserInfo](https://appstore.intelligentplant.com/ApiHelp/Api/GET-api-Resource-UserInfo)

*This returns info about the logged-in user.*

![](/dev/postman01.png)

If you attempt to execute this directly, you will receive an
unauthorized error like the following:

    {
      "Message": "Authorization has been denied for this request."
    }

This is because the App Store API is secured using OAuth2.

To prepare an authorization request, select "Authorization", type "OAuth
2.0" and click "Get New Access Token".

![](/dev/postman02.png)

You will be prompted for the following Authorization parameters:

| Auth URL         | https://appstore.intelligentplant.com/AuthorizationServer/OAuth/Authorize |
| ---------------- | ------------------------------------------------------------------------- |
| Access Token URL | https://appstore.intelligentplant.com/AuthorizationServer/OAuth/Token     |
| Client ID        | \[We'll give you this if you ask\]                                        |
| Client Secret    | \[We'll give you this if you ask\]                                        |
| Scope            | UserInfo                                                                  |
| Grant Type       | Authorization Code                                                        |

This returns an Access Token.

![](/dev/postman03.png)

Select "Use Token", try sending the API request again, and this time we
get the UserInfo result.

![](/dev/postman04.png)

#### Summary

In the above example we used Postman to simulate an external app
interacting with the App Store. Postman has been registered for use with
the App Store and obtained the required security credentials. For more
info, see **[Register your App](/Dev/Register%20your%20App)**.

Postman exposes the parameters required to make an OAuth2 authorization
request. Your application should execute this behind the scenes. For
more info, see **[App Store API Security
Overview](/Dev/App%20Store%20API%20Security%20Overview)**.

Finally, we used App Store as a means of authenticating users and
presenting user-information. However, there is an extensive API
available, including methods for user-account debiting and real-time
process-data interrogation. For more info, see **[App Store API
Documentation](https://appstore.intelligentplant.com/apihelp)**.
