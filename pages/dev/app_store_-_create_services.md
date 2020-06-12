# Create a Service Hub App

1.Log in into your account on [Intelligent Plant Industrial App
Store](https://appstore.intelligentplant.com/)

2.Navigate to "Applications" under "Developer" menu entry (if you
haven't registered to be a developer - follow this wiki on [How to
become a developer](/dev/app_store_-_become_a_developer)

![](/dev/1_appservice.png)

3.Click on "Add New Application" in the top right corner

![](/dev/3.png)

4.Provide a service name (e.g. Contoso Services) and a short
description.

![](/dev/6.png)

5.On application profile page you can skip straight to the bottom and
hit "Add Application" button.

![](/dev/2_appdev.png)

6.In app setting take a note of your Service App Id and Service App
Secret Key. Add a URL to "Authorized Redirect Urls" where your service
hub is hosted and append "signin-ip". For example
"<https://appstoredev.intelligentplant/serviceapphub/signin-ip>"

![](/dev/1.png)

# Modify Service Project

1\. Open web.config file and update ***ServiceAppId*** and
***ServiceAppSecret*** with the service app hub which you have created
in the steps above.

![](/dev/service_app_vs.png)

2\. In the example a SQL repository is used to store user tokens, you
could use the example model by modifying the connection string to use
your SQL server or you could implement your own solution/ repository.

3\. Make sure you call app store debit api action to charge the user for
the service.

4\. Modify the UI to fit your theme.

# Create service app

1.Follow steps 2 to 4 above to create a service application.

2.On "Add an Application Profile Step" (the one we skipped in step 5
above) add screenshots and/or a description for your service you are
going to provide.

![](/dev/3_servdev.png)

![](/dev/4_servdev.png)

3.Click "Add Application" to complete this step.

4.On application settings page add "Application Redirect Url". The URL
should be where your service hub is hosted, plus two parameters:
*"servicename"* - service name **must** match the name you gave your
application *cost* - how much your service costs

For example if service hub is hosted on
<https://intelligentplant.com/servicehub>, the "Application Redirect
Url" would look like this:

//<https://intelligentplant.com/servicehub/?servicename=Alarm%20Report%20Service&cost=33//>
