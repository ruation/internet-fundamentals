# IP (Internet Protocol) - Summary

The **Internet Protocol (IP)** is one of the most important protocols on the Internet. It is responsible for **addressing** and **routing** data so it can travel from one device to another across networks.

IP works by breaking data into small units called **packets** and delivering them to the correct destination using IP addresses.

## What an IP Address Is

An **IP address** is a unique identifier assigned to a device on a network. It allows devices to locate and communicate with each other.

Example of an IPv4 address:

```
192.168.1.10
```

Example of an IPv6 address:

```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```


## IPv4 vs IPv6

### IPv4
- Uses 32-bit addresses
- Written as four numbers separated by dots
- Example: `192.168.0.1`
- Limited number of available addresses (~4 billion)

### IPv6
- Uses 128-bit addresses
- Written in hexadecimal separated by colons
- Example: `2001:db8::1`
- Created to solve the IPv4 address shortage

## What IP Does

IP has two main responsibilities:

### 1. Addressing
Every device must have an IP address so data can be delivered to the correct destination.

### 2. Routing
IP helps routers decide the best path for packets to travel across the Internet.

When you send a message, IP adds a header to the packet containing:
- Source IP address
- Destination IP address

Routers read this information and forward the packet until it reaches its destination.

## Packet Delivery

IP does not guarantee that packets will arrive in order or arrive at all. It is considered a **best-effort protocol**.

This is why other protocols like **TCP** are used to provide reliability.

## Public IP vs Private IP

### Private IP
Used inside local networks (home, school, company).  
Common private ranges include:

- `192.168.x.x`
- `10.x.x.x`
- `172.16.x.x` to `172.31.x.x`

### Public IP
Used on the Internet and assigned by Internet providers.  
It is the address visible to websites and external services.

## Key Takeaways

- IP is responsible for addressing and routing data across networks.
- IP addresses identify devices on the Internet.
- IPv4 is older and limited; IPv6 is newer and supports many more addresses.
- IP is not reliable by itself, so TCP is often used with it.
