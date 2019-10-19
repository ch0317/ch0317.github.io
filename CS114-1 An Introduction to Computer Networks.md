---
typora-root-url: C:\Users\chenhao\Desktop\blog\ch0317.github.io
---

### CS114-1 An Introduction to Computer Networks![3-1](/images/cs114/3-1.png)



## The 4 Layer Internet Model

- link layer

  Delivers data over a single link between an end host and router, or between routers.

- network

  Delivers datagrams end-to-end. Best-effort delivery - no guarantees. Must use the Internet Protocol(IP)

- transport

  Guarantees correct , in-order delivery of data end-to-end. Controls congestion.

- application

  Bi-directional reliable byte stream between two applications, using application-specific semantic.(e.g. http, bit-torrent)

![1571473793701](/images/cs114/3-2.png)

The Network Layer almost can only choose IP protocol.



#### The Internet Protocol(IP)

![1571474138037](/images/cs114/3-3.png)

1.  IP datagrams consist of a header and some data
2. When the transport layer has data to send, it hands a Transport Segment to the Network layer below.
3. The network layer puts the transport segement inside a new IP datagram.
4. IP's job is to deliver the datagram to the other end.

![1571478781844](/images/cs114/4-1.png)

1. Tried to prevent packets looping forever.
2. Will fragment packets if they are too long.
3. Uses a header checksum to reduce chances of delivering datagram to wrong destination.
4. Allows for new versions of IP.
5. Allows for new options to be added to header.

![1571487608308](/images/cs114/4-2.png)



### summary

We use IP every time we send and receive datagrams.

IP provides a deliberately simple service:

- Datagrams
- best effort
- unreliable
- connectionless

