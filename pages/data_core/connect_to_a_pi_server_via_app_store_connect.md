# Connect to a PI Server via App Store Connect

Before you can configure an PI Server connection, App Store Connect must
be running. If you have not done this yet, refer to: [How to Connect
your Data to the App
Store](/Data_Core/How%20to%20Connect%20your%20Data%20to%20the%20App%20Store)

## To configure a PI Server connection

1\. Open the following link:
<https://appstore.intelligentplant.com/gestalt/admin/remotehosts>

![](/data_core/piconfig00.png)

2\. The Remote Hosts page shows your App Store Connect instance. Select
"Data Sources".

![](/data_core/piconfig01.png)

3\. Select "Create New Data Source"

![](/data_core/piconfig02.png)

4\. Select Type "OSISoft PI" and provide a name for your Data Source
connection.

![](/data_core/piconfig03.png)

5\. Configure your PI Server settings. Most of the default settings
should suffice, however you will need to enter details for "Server",
"Username" and "Password". Finally, set the "Disabled" setting to
"False".

![](/data_core/piconfig04.png)

*Your PI App Store Connection is now available.*

## Test your PI Server connection

A quick test of your connection is available from the above
administration pages. Return to the "Data Sources" page (step 2 above)
and choose "Tags".

![](/data_core/piconfig05.png)

The Tags page allows you to query available tags on your PI Server.

![](/data_core/piconfig06.png)
