# TCP (Transmission Control Protocol) - Summary

The **Transmission Control Protocol (TCP)** is a core protocol of the Internet used to provide **reliable communication** between devices. It is commonly used when data must arrive correctly and in the right order, such as when loading websites, sending emails, or downloading files.

TCP works together with IP, and this combination is often called the **TCP/IP model**.

## What TCP Does

TCP is responsible for:

- Ensuring data is delivered correctly
- Sending packets in the correct order
- Detecting lost packets and retransmitting them
- Preventing congestion and controlling data flow

Unlike IP, TCP guarantees reliable delivery.

## TCP Connection (Three-Way Handshake)

Before sending data, TCP establishes a connection using a process called the **three-way handshake**:

1. **SYN**  
   The client sends a request to start a connection.

2. **SYN-ACK**  
   The server acknowledges the request and responds.

3. **ACK**  
   The client confirms, and the connection is established.

After this handshake, both sides can safely exchange data.

## Data Transmission and Reliability

TCP splits data into segments and adds important information such as:

- Sequence numbers (to keep packets in order)
- Acknowledgements (to confirm delivery)
- Error checking (to detect corruption)

If a segment is lost or arrives damaged, TCP will request it again.

## Flow Control

TCP uses a mechanism called **flow control** to avoid sending too much data at once. This prevents the receiver from being overwhelmed.

## Congestion Control

TCP also includes **congestion control**, which helps reduce traffic problems on the network by adjusting the speed of transmission when the network is overloaded.

## TCP vs UDP

TCP is often compared to UDP (User Datagram Protocol):

- **TCP**: reliable, ordered, connection-based
- **UDP**: faster, but not reliable, connectionless

TCP is used when accuracy is important, while UDP is used when speed matters more (like streaming and online games).

## Key Takeaways

- TCP ensures reliable and ordered delivery of data.
- It establishes connections using the three-way handshake.
- It detects errors and retransmits lost packets.
- TCP is essential for web browsing, file transfers, and email.
