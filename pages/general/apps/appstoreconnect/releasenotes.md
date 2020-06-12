# App Store Connect Release Notes

This page describes the release notes for [App Store
Connect](https://appstore.intelligentplant.com/Home/AppProfile?appId=a73c453df5f447a6aa8a08d2019037a5).
Your App Store Connect will automatically download the update. You can
configure the update schedule for your App Store Connect by following
the instructions available
[here](https://appstore.intelligentplant.com/wiki/doku.php?id=data_core:app_store_connect_updates).

### 2020-05

This release contains the following changes:

  - Improvements to the Alarm Analysis data source driver in preparation
    for the next Alarm Analysis app release.
  - Edge Historian tags can be configured to record the current value
    only (i.e. no history).
  - New aggregate functions supported in Edge Historian:
    \`AnnotationCount\`, \`Count\`, \`PercentGood\`, \`PercentBad\`,
    \`Range\`, \`Delta\`, \`StdDev\`, \`Variance\`
  - \`Range\` aggregate function now supported in OSIsoft PI and AF
    drivers.
  - Improvements to automatic reconnection in PI and AF drivers.
  - Fix for older versions of IE when browsing tags in the App Store
    Connect UI.
  - Improvements to the App Store Connect trending UI.
  - Miscellaneous small improvements.

### 2020-03

This release contains the following changes:

  - Improvements and bug fixes related to Alarm Analysis data import and
    reporting queries.
  - Improvements and bug fixes related to the restart of data stream
    rules (used to transfer real-time data from a source data source to
    a destination data source such as App Store Connect's Edge
    Historian). 
  - Fixes for some C\# script tag templates that called back into Data
    Core for historical data.
  - JavaScript-based script tags are now deprecated in favour of
    C\#-based script tags.
  - A new driver for [Aspentech
    IP.21](https://www.aspentech.com/en/products/msc/aspen-infoplus21),
    capable of interfacing with its HTTP-based REST API. This driver is
    in preview and will receive improvements over the coming months. 
  - Miscellaneous bug fixes.
