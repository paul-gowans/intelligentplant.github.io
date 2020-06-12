# Big Data Event Source/Sink

## Overview

Intelligent Plant's **Big Data Service** (part of the App Store Connect
installation) is employed by Data Core as an event source and sink.
Using it as a sink can be useful if we wish to define a local collecting
area.

For example, if we're monitoring an OPC data-source, our ultimate
destination may be a Alarm Analysis. We can start collecting data
immediately, while fine-tuning Alarm Analysis import rules.

The data is stored to Big Data in monthly indices. The index name is
derived automatically from event source.

## Requirements

  - Big Data Windows Service must be running

### Data Storage

If using Big Data Event Sink, be sure to have sufficient disk space. If
dealing with high volumes of data, consider contacting Intelligent Plant
to request a custom installation of App Store Connect employing a
dedicated data drive.
