# App Store API Security Overview

Before an application can interact with the ***App Store API*** and
access data that belongs to a User, it must obtain explicit
authorization from said User. The App Store provides as OAuth2
Authorization Service to facilitate this action. A non-technical summary
of the security flow is as follows:

### Step 1. User Authentication

    Is the user who they claim to be?

Any interaction between a user and the App Store must be authenticated.
If the user is not authenticated, App Store will redirect your request
to a LinkedIn log-in page.

![](/dev/apisecurity01.png) ![](/dev/apisecurity02.png)

This means the App User must have a LinkedIn account and approve the
AppStore request to access personal data from LinkedIn.

If user agrees, we proceed to App Authentication.

### Step 2. App Authentication

    Is the App who they claim to be?

We only trust registered Apps. When you register an App with the App
Store, you are assigned:

``` 
 * An AppId - a unique reference for your application
 * An AppSecret - a secret key never to be shared
```

And for web app developers, we require a record of

``` 
 * the Web App %%URL%%(s)
  
```

We will only trust internet requests from recognized domains.

### Step 3. App Authorization

    Is the User okay for the App to act for them?

Each ***App Store API*** method has one or more security pre-requisites.
For instance, the method to debit a user's App Store Credit Account is
only available if the user has authorized the App to make “Account
Transaction” requests on their behalf.

Thus, the App must tell the App Store which privileges it requires. The
App Store then prompts the user to Authorize this request.

![](/dev/apisecurity03.png)

### Step 4. Access Token

Once steps 1-2-3 above are satisfied, the App Store will issue an access
token - opening up the ***App Store API*** and allow your App to fully
interact with the App Store.

``` 
 * The //**App Store %%API%%**// Methods: https://appstore.intelligentplant.com/apihelp
```
