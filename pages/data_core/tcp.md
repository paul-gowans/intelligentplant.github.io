# TCP Event Source and Sink

Data Core objects "TCP Event Source" and "TCP Event Sink" provide a
mechanism to route Data Core event messages between Data Core Nodes,
potentially crossing network boundaries and firewalls.

``` 
 A Data Core Node is an instance of Intelligent Plant's
 data-routing and data-access software operating as a Windows
 service. App Store Connect is a type of Data Core Node
 pre-configured to work with the App Store.
```

## When to use TCP Event Sink and Source

Data Core's Event Source and Sink subscription model is designed to
relay messages reliably within a Data Core Node. Using a Data Bridge (a
means of registering Data Core Nodes with one another) this model can be
extended between Data Core Nodes. However, a Data Bridge allows one Node
to employ the API of the other. In dealing with data communication from
a high-security militarized network any communication to an exposed
application API is not permissable.

The TCP Event Sink and Source provides a more suitable method for
crossing network boundaries: a strictly data-only channel with minimal
firewall reconfiguration required.

## Data Core Components

![](/data_core/datacorediagram.png)

In the above diagram, Alarms & Events (A\&E) are transmitted from the
PCN to the PIN via a serial feed. (In terms of physical architecture, a
Serial Port to TCP Converter would be employed).

The A\&E Collector may be any Data Core Event Sink that writes data to a
repository (for example, MSMQ Event Sink, Big Data Event Sink, etc).

A subscription is set from an A\&E Collector to the TCP Event Sink,
which in turn relays messages to the remote TCP Event Source.

Finally, a collector on the remote Data Core node persists incoming
messages.

If a problem is encountered at any point along the chain, events are
resubmitted from PIN collector to BN collector.

## Firewall Configuration

  - PIN:BN Firewall requires TCP Port 11000 (configurable) open to
    outbound traffic.

## Secure TCP Connection

Connections between the TCP Event Sink and Source are only permitted if
an ***autheticated***, ***encrypted*** and ***signed*** communication is
established.

  - TCP authentication on Windows Server 2012 or above (recommended)
    uses the Kerebos protocol and requires a system account (see "System
    Account Requirements" below).

<!-- end list -->

  - Data signing helps to protect the integrity of the data. namely, it
    helps the recipient determine whether the data has been tampered
    with while in transit.

<!-- end list -->

    *Encryption protects the privacy of the data. It helps to ensure that while data is in transit it cannot be deciphered by third parties.

## System Account Requirements

For TCP authentication, the TCP Client supplies credentials for the TCP
server to verify. We recommend creating a local windows account defined
on the computer hosting the TCP Event Source.

![](/data_core/tcp_02.png)

The username and password is then supplied in the TCP Event Sink
configuration.

![](/data_core/tcp_03.png)

NB. Sensitive Data Core configuration is encrypted.
