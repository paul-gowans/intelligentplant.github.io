# App Store Connect Updates

Once installed, App Store Connect receives software updates distributed
via the Intelligent Plant NuGet service - *a mechanism for pushing
update packages to App Store Connections*.

By default, updates are distributed automatically from the "stable"
NuGet feed. But this can be modified to update on demand, and/or from an
alternative NuGet feed.

## Modify "App Store Connect" NuGet Feed

The following NuGet feeds are available:

| Feed   | URL                                                  | Description                                                                                                                                             |
| ------ | ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Stable | <https://packages.intelligentplant.com/stable/nuget> | Official production release.                                                                                                                            |
| Beta   | <https://packages.intelligentplant.com/beta/nuget>   | **Pre-release:** Beta versions have gone through in-house alpha testing and are generally fairly close in look, feel and function to the final product. |
| Canary | <https://packages.intelligentplant.com/canary/nuget> | **Pre-release:** Canary versions contain the latest functionality, but may not be carefully tested.                                                     |

To modify the NuGet Feed:

1\. In Windows Services, stop **Intelligent Plant Data Core Service**.

2\. Open configuration file: `%ProgramFiles%\Intelligent Plant\Data
Core\DataCore.ApplicationHost.exe.config`.

3\. Modify app setting "appStoreRepositoryPath": `<add
key="applicationHostEngine.appStoreRepositoryPath" value="[Enter NuGet
URL here]" />
`

4\. If changing to a **pre-release** feed (e.g. Beta or Canary), perform
steps 4.1 and 4.2:

4.1. Open configuration file: `%ProgramData%\Intelligent Plant\Data Core
Application Host\Service\Data\Data Core Application
Host.DataStoreApplicationManager.Applications.data`.

4.2. Modify `AllowPreReleasePackages` setting:
`"AllowPreReleasePackages": true,
`

5\. In Windows Services, restart **Intelligent Plant Data Core
Service**.

## Modify "App Store Connect" Update Check Schedule

By default, App Store Connect automatically updates when new software
packages are available. This results in short periods of downtime.

Updates are usually \[1\] deployed on Fridays business during UK
business hours. If this is not convenient, update checks can be
rescheduled as follows:

1\. In Windows Services, stop **Intelligent Plant Data Core Service**.

2\. Open configuration file: `%ProgramFiles%\Intelligent Plant\Data
Core\DataCore.ApplicationHost.exe.config`.

3\. Modify app settings for `checkForUpdatesSchedule` and
`checkForUpdatesOnStartup`:

    <add key="applicationHostEngine.checkForUpdatesSchedule" value="0 0 12 ? * SAT *" />
    <add key="applicationHostEngine.checkForUpdatesOnStartup" value="false" />

The schedule is specified as a [CRON](http://www.cronmaker.com/)
schedule (for example, "0 0 12 ? \* SAT \*" checks for updates every
Saturdays at midday).

4\. In Windows Services, restart **Intelligent Plant Data Core
Service**.

## Disable "App Store Connect" Automatic Updates

To disable automatic updates altogether (not recommended):

1\. In Windows Services, stop **Intelligent Plant Data Core Service**.

2\. Open configuration file: `%ProgramData%\Intelligent Plant\Data Core
Application Host\Service\Data\Data Core Application
Host.DataStoreApplicationManager.Applications.data`.

3\. Modify `AutoUpdate` setting:

\<code\> "AutoUpdate": false, \</code\>

4\. In Windows Services, restart **Intelligent Plant Data Core
Service**.

1.  Stable packages may be released outside usual deployment schedules
    if urgent. Pre-release packages may be deployed at any time.
