# Data Core: Create an Event Subscription

Event Sources push events to subscribed Event Sinks.

Event Sinks subscribe to Event Sources to process events. For example,
save event to a log or database, send an email, etc…

The example below shows a subscription between a SQL Event Source (which
collects data from SQL Server) and Big Data Event Sink (which stores
data to Elasticsearch).

For a full collection of Data Core components and configuration, see
[Data Core Components](/data_core/data_sources)

## Open Data Core

1\. Log onto application server hosting App Store Connect

2\. Open App Store Connect: <http://localhost:2006/service>

3\. Select “Configure Data Core”

![](/data_core/datacorehome.png)

If the menu bar does not list the options above, check if you have [Data
Core Administrator
Privileges](/app_store_connect/data_core_administrator_privileges)

## Create an Event Source

![](/data_core/createeventsrc.gif)

## Create an Event Sink Subscription

![](/data_core/createeventsnk.gif)
