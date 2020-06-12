# IAS Power BI Connector Release Notes

This page describes the release notes for [Power BI
Connector](https://appstore.intelligentplant.com/Home/AppProfile?appId=a73c453df5f447a6aa8a08d2019037a5).
Your Power BI will automatically download updated connector when a new
release is published by Microsoft.

### 2020-06 (Power BI June update)

This release contains the following changes:

  - Introduced new **Get Snapshot** data function to retrieve the
    current tag(s) value.
  - Added new **Get Plot** data to perform a processed data request
    using PLOT function.
  - Added new **Get Processed** data to perform a processed or
    aggregated data query.
  - Added new **Get Raw** data to perform a raw data query.
  - Every function has an optional parameter to indicate which data type
    to use and display the results. For example, some digital tags or
    A\&E data tags might have a text value as well as a numerical value.
    The numerical value is used by default, if unavailable - text value
    will be used.
  - New Power Platform API was introduced that will help us transfer the
    data faster and more efficiently whilst keeping the same
    high-security standards.
  - Under the hood fixes and improvements.
