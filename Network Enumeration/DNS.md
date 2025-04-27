## What is DNS Enumeration?

**DNS Enumeration** is a recon (information gathering) technique where you try to uncover information in the target's Domain Name System (**DNS**) infrastructure. <bn>
In other words, you are trying to scrape subdomains, DNS records, IP addresses, MX (mail) servers and other critical information under the target domain.

#### Purpose:

    Finding subdomains (such as admin.target.com, dev.target.com)
    
    Discovering mail servers (MX records)
    
    Analyze DNS structures (A, AAAA, CNAME, TXT records)
    
    Sometimes finding an opportunity to infiltrate through incorrectly configured records

## DNS Enumeration Methods

#### Zone Transfer Attack (AXFR)

You try to pull full records from the DNS server. In case of incorrect configuration, a complete sitemap is generated.

#### Subdomain Bruteforce

Using Wordlist, you can brute-force possible subdomains (admin., dev., test. etc.).

#### DNS Record Discovery
Query A, AAAA, CNAME, TXT, MX records. Especially TXT records sometimes contain confidential information (e.g. AWS IDs).

#### Reverse DNS Lookup
Try to resolve domain names from IP addresses. It is especially useful for large IP blocks.

#### Google Dorking + DNS

Use dork to find DNS information or subdomains via Google ```(site:*.target.com)```.

#### Certificate Transparency Logs
Collect subdomains registered with SSL certificates (from sites like crt.sh).

## Tools Used
- dig (the most classic tool for Linux)
- nslookup
- dnsenum
- fierce
- amass
- subfinder
- crt.sh (looking at cert logs over the web)
- massdns (for very large bruteforce jobs)