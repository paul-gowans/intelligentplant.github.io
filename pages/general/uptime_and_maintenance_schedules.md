# Uptime and Maintenance Schedules

The Industrial App Store is a distributed architecture consisting of
Apps, APIs, Data Connections and Data Sources. Although we aim to limit
disruption to App Store services, occasional maintenance is required.

## Notifications


  <span style="font-size:large">
    <a href="https://share.hsforms.com/1_deJNPacTtWO60z-KYW7Ow45ie5" target="_blank">Click here to sign up for scheduled maintenance email notifications.</a>
  </span>

## Maintenance Policy

Below is our policy for managing uptime.

  - **Production**  
    Intelligent Plant \[1\] generally schedule updates and maintenance
    for **Fridays 10:00-14:00 British Local Time**.  
    Exceptions may be made for high priority fixes.  
    Refer to Maintenance Calendar for upcoming events.

<!-- end list -->

  - **Pilot / Beta / Canary**  
    Pre-production apps and services may be updated at any time without
    notice.

<!-- end list -->

  - **App Store Connects**  
    App Store Connect updates are distributed via NuGet package feeds.
    Although we prepare package feed updates for last Friday of every
    month, you can control *if* and *when* to collect them. For more
    detail, refer to [App Store Connect
    Updates](/data_core/App%20Store%20Connect%20Updates).

## Maintenance Calendar

| App                  | Impact Detail                                                                                                                                          | Maintenance Window                | Anticipated Downtime |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------- | -------------------- |
| Gestalt PnID & Trend | Deployment is for client side changes only and will not cause any downtime.                                                                            | Fri 12 Jun 2020 12:00 - 13:00 GMT | N/A                  |
| Alarm Analysis       | During the deployment, the Alarm Analysis website will be briefly unavailable. In such circumstances, we advise users to wait a moment then try again. | Fri 12 Jun 2020 12:00 - 13:00 GMT | 20 mins              |

## Release Notes

Release notes for the Industrial App Store and various Intelligent Plant
apps can be viewed using the links below:

  - [Industrial App Store
    Portal](https://appstore.intelligentplant.com/wiki/doku.php?id=general:apps:appstore:releasenotes)
  - [App Store
    Connect](https://appstore.intelligentplant.com/wiki/doku.php?id=general:apps:appstoreconnect:releasenotes)
  - [Alarm
    Analysis](https://appstore.intelligentplant.com/wiki/doku.php?id=general:apps:alarmanalysis:releasenotes)
  - [Gestalt
    PnID](https://appstore.intelligentplant.com/wiki/doku.php?id=general:apps:gestaltpnid:releasenotes)
  - [Gestalt
    Trend](https://appstore.intelligentplant.com/wiki/doku.php?id=general:apps:gestalttrend:releasenotes)
  - [Sequence of Events Explorer
    (SOEx)](https://appstore.intelligentplant.com/wiki/doku.php?id=general:apps:soex:releasenotes)
  - [IAS Power BI
    Connector](https://appstore.intelligentplant.com/wiki/doku.php?id=general:apps:powerbi:releasenotes)

<!-- end list -->

1.  The Industrial App Store serves apps from multiple vendors. For
    non-Intelligent Plant apps, please refer to directly to the vendor
    for details of their update schedules.
