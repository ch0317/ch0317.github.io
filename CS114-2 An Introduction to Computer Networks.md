---
typora-root-url: ./
---



# CS114-2 An Introduction to Computer Networks

![1572318699919](images/cs114/15-1.png)

- The TCP layer at Host A can close the connection by sending a FIN message
- Host B acknowledges that no longer has data to send and stops looking for new data from A. This closes the data stream from A to B. But B might still have new data to send to A and is not ready to close down the channel from B to A. So the message from B to A carrying the ACK message can also carry new data.
- B finishes sending data to A, and send its own FIN to tell A they can close the connection.
- A send ACK to a full close.

### The TCP Service Model

- Stream of bytes: Reliable byte delivery service


- Reliable delivery: 
  1. Acknowledgments indicate correct delivery.
  2. Checksums detect corrupted data.
  3. Sequence numbers detect missing data.
  4. Flow-control prevents overrunning receiver.
- In-sequence: Data delivered to application in sequence transmitted
- Congestion Control: Control network congestion.



![1572328242058](/images/cs114/15-2.png)

### The UDP Sevice Model

![1572328866024](/images/cs114/15-3.png)

- Connectionless: No connection established
- Datagram Service: Packets may show up in any order.
- Self contained datagram
- Unreliable delivery:
  1. No acknowledgments.
  2. No mechanism to detect missing or mis-sequenced datagrams.
  3. No flow control.

#### The Internet Control Message Protocol(ICMP) Service Model

Internet Control Message Protocol(ICMP)

- Communicates network layer information between end hosts and routers
- Reports error conditions
- Helps us diagnose problems

![1572332029758](/images/cs114/15-4.png)

![1572332722474](/images/cs114/15-5.png)



