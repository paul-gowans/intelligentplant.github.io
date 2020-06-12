# How to Connect your Data to the App Store

Connecting to the **App Store** allows you to use your own data sources
(including OSIsoft PI, OPC, and more) with **App Store** applications
such as **Gestalt Trend** and **PnID**. It does this via a secure
outgoing connection. It will not compromise the security of your server
or network.

To get up and running, you need to undertake the following tasks:

1.  [\#Install App Store Connect](#Install%20App%20Store%20Connect)
2.  [\#Configure App Store Connect](#Configure%20App%20Store%20Connect)
3.  [\#Connect Data Sources](#Connect%20Data%20Sources)

Each step is explained in detail below:

## Install App Store Connect

The first step in connecting your data to the App Store is downloading
and installing App Store Connect.

1.  Go to the [App Store](http://appstore.intelligentplant.com), log-in
    and select **My Account \> Get Connected**
2.  Click on **Download App Store Connect**
3.  Once downloaded, start the Installer (right click and select "run as
    administrator").

The installer takes you through the following steps. We recommend you
choose the default **Typical** set-up option.

![](/data_core/installdatacore01.png)
![](/data_core/installdatacore02.png)
![](/data_core/installdatacore04.png)

## Configure App Store Connect

Once installed, open the configuration page
(<http://localhost:2006/Service>)

1\. Authorize App Store Connect by selecting "Log In". Your personal
details are authenticated by LinkedIn and then you will be prompted to
approve App Store Connect's request to run on your behalf.

![](/data_core/configureasc01.png) ![](/data_core/configureasc04.png)

3\. Once credentials are set, start it up.

![](/data_core/configureasc03.png)

## Connect Data Sources

To connect Data Sources, we need to configure Data Core.

1\. Open the App Store Connect configuration page
(<http://localhost:2006/Service>) then select "Configure Data Core"

![](/app_store_connect/asc_00.png)

2\. From top navigation, select "Real Time Data \> Data Sources".

**NB.** Only Data Core Administrators can configure data-sources. If
"Real Time Data" is not present in the menu navigation, refer to [Data
Core Administrator
Privileges](/app_store_connect/Data%20Core%20Administrator%20Privileges).

![](/app_store_connect/asc_01.png)

3\. Select "Create a Data Source"

![](/app_store_connect/asc_03.png)

You will be presented with a list of available datasources - each with
it's own properties and settings. For driver specific information, refer
to [Advanced Data Core
Configuration](/data_core/Advanced%20Data%20Core%20Configuration).

[Get in touch](http://www.intelligentplant.com/contact.html) and let us
know about the data you're connecting.
