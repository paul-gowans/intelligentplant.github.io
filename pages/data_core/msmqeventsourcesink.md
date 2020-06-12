# MSMQ Event Source/Sink

## Overview

MicroSoft Message Queue is employed by Data Core as a event source and
destination. Using it as a sink can be useful if we wish to define a
local collecting area.

For example, if we're monitoring an OPC data-source, our ultimate
destination may be a remote instance of Alarm Analysis. However, before
we commence sending it out across networks we may wish to employ a local
collecting area - such as MSMQ.

It is assumed MSMQ contains Data Core Event messages.

## Configuration

  - Message Queue Type: Currently, only access to private queues on
    local server are supported.
  - Server Name: As above, only local supported.
  - Queue Name
