## DNS (Domain Name Server)

it's like a wallet, your ID, your credit card is a domain and your wallet is a DNS.

### IMPORTANT!!

www.google.com is not a **DNS** *grrr* 😾

---
**DNS**: directs internet traffic by converting the domain names that people type into their web browsers into the IP addresses corresponding to these sites. \
DNS is of great importance because the numerical IP addresses of resources on the internet can often be complex and difficult to remember.

## What is BIND?

The Berkeley Internet Name Domain (BIND) is one of the most popular DNS servers in use today. It was developed at the University of Berkeley in the 1980s and is currently in version 9. BIND is an open source system available under the Mozilla Public License, free to download and use.

BIND can be used to cache a DNS server or run an authoritative name server, and provides features such as load balancing, notification, dynamic update, split DNS, DNSSEC, IPv6.

## DNS Zone

Information about domains in the DNS database is stored in zone files. A zone file consists of directives and resource records. Directives tell the name server to perform tasks or apply zone-specific settings. Resource records define the parameters of the zone and store host information. Directives are optional, but resource records are required. A resource record has the following fields (Some fields are optional depending on the type):

- Name: Domain name or IP address
- TTL: Time to live, the maximum time a record will be cached before checking for a new one
- Class: Always IN for Internet
- Type: Record type
- Data: Varies by record type

- A: IPv4 address
- CNAME: Canonical name or alias
- MX: Mail exchange, specifies the destination of mail sent to the domain
- NS: Nameserver, specifies the system that provides DNS records for the domain
- PTR: Maps an IP address to a domain name for reverse name resolution
- SOA: Start of authority, specifies the beginning of a zone