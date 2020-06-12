![<https://azimuth.intelligentplant.com>](/azimuth/azimuth_100.png)

``` 
                                         ==== Intelligent Plant Azimuth ====
```

#### Ensure:

    *efficient maintenance scheduling on major pieces of rotating equipment.
    *reliability
    *downtime tracking (planned/unplanned)

-----

### Prerequisites

  - **Alarm Analysis** (*type*) data source. Source data source, will be
    used to define equipment events. Azimuth will use these event
    definitions to monitor equipment.
  - **Edge Historian** data source. Target data source, Azimuth will use
    this datasource to store analysis results.

-----

### Getting started

Azimuth uses asset and equipment hierarchical structure. One or more
pieces of equipment can be defined on an asset. For example:

![<https://azimuth.intelligentplant.com>](/azimuth/asseteqhier.png)

1.  Adding an asset (subscription)
2.  Adding equipment

-----

### Known issues

  - Creating a piece of equipment with a duplicate name on the same
    target datasource will cause to override previous equipment
    totaliser tag data.
