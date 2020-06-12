# Data Core: Stand-Alone Installation

Data Core is Intelligent Plant's data connectivity suite.

*App Store Connect* is an instance of Data Core pro-configured for
connecting data to the Intelligent Plant's app store, but if can also be
installed and configured to move data across networks or connect with
locally deployed applications.

### System Requirements

System requirements are the same as App Store Connect.

  - [System Requirements](/App_Store_Connect/System%20Requirements)

Alternatively, if your server has an outgoing internet connection,
consider creating a new repo configured to connect to the App Store
Nuget feed.

![](/data_core/datacoreinstall06.png)

### Installation

1\. Download Installer and latest stable Node Package

  - [Installer.DataCore.StandAlone.exe](https://appstore.intelligentplant.com/nuget/downloads/Installer.DataCore.StandAlone.exe)
  - [DataCore.ApplicationHost.Node.nupkg](https://appstore.intelligentplant.com/NuGet/api/v2/package/DataCore.ApplicationHost.Node/3.2.15000)

2\. Run Installer

3\. Copy package to packages folder

  - %ProgramFiles%\\Intelligent Plant\\Data Core\\Packages

4\. Open Data Core website

  - <http://localhost:2006/Service>
  - Click "Create Application"

![](/data_core/datacoreinstall01.png)

5\. Configure the following properties:

  - Repository: local
  - Name: Data Core Node
  - Apply updates: checked
  - Enabled: checked
  - Click “Add Application”

![](/data_core/datacoreinstall02.png)

6\. The Data Core "Application" starts automatically. Now open the
Application.

![](/data_core/datacoreinstall03.png)

7\. Select "Update License"

![](/data_core/datacoreinstall04.png)

8\. Request a Data Core license key from Intelligent Plant, specifying
Machine Id.

  - Once supplied, enter then click “Update License”.

![](/data_core/datacoreinstall05.png)

9\. Finally, reboot the server.

*Intelligent Plant Data Core is now running on your server.*
