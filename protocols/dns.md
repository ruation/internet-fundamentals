# DNS (Domain Name System) - Summary

The **Domain Name System (DNS)** is a system that translates **domain names** (like `google.com`) into **IP addresses** (like `142.250.184.14`). Since computers communicate using IP addresses, DNS works like the "phonebook of the Internet".

## Why DNS Exists

Humans prefer to remember names such as `github.com`, but networks need IP addresses to locate servers. DNS allows users to access websites using easy-to-read names instead of numbers.

## How DNS Works (Step-by-Step)

When you type a website name into your browser, DNS resolution usually happens like this:

1. **Browser Cache**
   - The browser checks if it already knows the IP address for that domain.

2. **Operating System Cache**
   - If the browser doesn't have it, the computer checks its own DNS cache.

3. **DNS Resolver (ISP or Public DNS)**
   - If the IP is still unknown, the request is sent to a DNS resolver (usually from your ISP or services like Google DNS or Cloudflare DNS).

4. **Root DNS Server**
   - The resolver contacts a root server, which directs it to the correct Top-Level Domain (TLD) server (like `.com`, `.org`, `.net`).

5. **TLD Server**
   - The TLD server points the resolver to the domain's authoritative DNS server.

6. **Authoritative DNS Server**
   - This server contains the real DNS records for the domain and responds with the correct IP address.

7. **Response Returned**
   - The resolver sends the IP address back to your computer.
   - The browser can now connect to the web server using that IP.

## TLD (Top-Level Domain)

TlDs tell users the general purpose of the service behind the domain name. Examples:
- .com: the most popular, initially was for "commerce"
- .us, .br: this for country's
- .gov: only government departments can use this.
- .edu: use by educational and academic institutions.

## DNS Caching

DNS uses caching to improve speed and reduce traffic. When a DNS resolver receives an answer, it stores it for a period defined by the **TTL (Time To Live)** value.

## Common DNS Record Types

- **A Record**: Maps a domain name to an IPv4 address.
- **AAAA Record**: Maps a domain name to an IPv6 address.
- **CNAME Record**: Points one domain name to another domain name.
- **MX Record**: Specifies mail servers for a domain.
- **TXT Record**: Stores text information (often used for verification and security).

## Key Takeaways

- DNS converts domain names into IP addresses.
- It involves multiple servers: resolver, root, TLD, and authoritative servers.
- Caching makes DNS faster and reduces repeated lookups.
- DNS is essential for making the internet easier to use.
