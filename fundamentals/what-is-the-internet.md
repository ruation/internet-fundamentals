# The Internet - Basic Concepts

## Network

First of all, we need to understand what a network is. A network is a group of computers or devices that are connected to each other.

You can think of it like a web, where nodes are connected. However, not every node is directly connected to every other node.

- **The Internet is a network of networks.**

At its core, the Internet is a global system of interconnected routers. These routers are responsible for directing traffic between different devices and networks.

When you send data over the Internet, it is broken into small pieces called packets. These packets travel from your device through multiple routers until they reach their destination.

Each router examines the packet and forwards it to the next router along the path. This process continues until the packet reaches its final destination.

## Browsers


A [**web browser**](browsers.md) is an application that allows users to access and interact with websites on the Internet. Examples of popular browsers include **Google Chrome**, **Mozilla Firefox**, **Microsoft Edge**, and **Safari**.

Browsers act as a bridge between the user and the web. They request resources from web servers and display them in a human-readable format.

## Protocols

Protocols are rules that ensure data is sent and received correctly over the network.

- **Internet Protocol (IP):** Responsible for addressing and routing packets to their destination.
- **Transmission Control Protocol (TCP):** Ensures that packets are delivered reliably and in the correct order.
- [**Domain Name System (DNS):**](../protocols/dns.md): The "phonebook of the Internet", that translates URL into IP Adress.
- [**Hypertext Transfer Protocol (HTTP)**](../protocols/http.md): Responsible for communication between the client (browser) and the server.
- **SSL/TLS:** Provides security through encryption.

## Basic Concepts and Terminology

- **Packet:** A small unit of data transmitted over the Internet.
- **Router:** A device that forwards data between networks.
- **Domain Name:** A human-readable name used to identify a website, such as `github.com`.
