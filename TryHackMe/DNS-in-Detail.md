# DNS in Detail

Table of Contents

- [DNS in Detail](#dns-in-detail)
  - [Overview](#overview)
  - [Domain Hierarchy](#domain-hierarchy)
    - [TLD (Top-Level Domain)](#tld-top-level-domain)
    - [Second-Level Domain](#second-level-domain)
    - [Subdomain](#subdomain)
  - [DNS Record Types](#dns-record-types)
  - [Making a Request](#making-a-request)

## Overview

**DNS (Domain Name System)** provides a simple way for us to communicate with devices on the internet without remembering complex numbers.

Much like every house has a unique address for sending mail directly to it, every computer on the internet has its own unique address to communicate with it called an IP address. An IP address looks like the following `104.26.10.229`, 4 sets of digits ranging from 0 - 255 separated by a period.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20200822065029/UntitledDiagram.png" width="400" alt="domain name system"/>

## Domain Hierarchy

### TLD (Top-Level Domain)

A **TLD** is the rightmost part of a domain name, like `.com` in `tryhackme.com`. There are two types:

- **gTLD (Generic TLD):** Originally indicated the domain's purpose (e.g., `.com` for commercial, `.org` for organizations, `.edu` for education, `.gov` for government).
- **ccTLD (Country Code TLD):** Denotes geographic location (e.g., `.ca` for Canada, `.co.uk` for the UK).

Due to demand, many new gTLDs exist, like `.online`, `.club`, `.biz`, and more.

### Second-Level Domain

In `tryhackme.com`, **tryhackme** is the **Second-Level Domain** (SLD). When registering a domain, the SLD:

- Must be **63 characters or less** (plus the TLD).
- Can include **a-z**, **0-9**, and hyphens, but **cannot** start/end with hyphens or have consecutive ones.

### Subdomain

A **subdomain** precedes the Second-Level Domain, separated by a period (e.g., `admin` in `admin.tryhackme.com`). Subdomains follow the same rules as SLDs:

- Up to **63 characters** using **a-z**, **0-9**, and hyphens (no starting/ending hyphens or consecutive ones).
- Multiple subdomains can be chained (e.g., `jupiter.servers.tryhackme.com`), but the total length must not exceed **253 characters**.
- There's **no limit** to the number of subdomains you can create.

## DNS Record Types

DNS isn't just for websites though, and multiple types of DNS record exist. We'll go over some of the most common ones that you're likely to come across.

- **A Record**: These records resolve to IPv4 addresses, for example 104.26.10.229

- **AAAA Record**: These records resolve to IPv6 addresses, for example 2606:4700:20::681a:be5

- **CNAME Record**: These records resolve to another domain name, for example, TryHackMe's online shop has the subdomain name store.tryhackme.com which returns a CNAME record shops.shopify.com. Another DNS request would then be made to shops.shopify.com to work out the IP address.

- **MX Record**: These records resolve to the address of the servers that handle the email for the domain you are querying, for example an MX record response for tryhackme.com would look something like alt1.aspmx.l.google.com. These records also come with a priority flag. This tells the client in which order to try the servers, this is perfect for if the main server goes down and email needs to be sent to a backup server.

- **TXT Record**: TXT records are free text fields where any text-based data can be stored. TXT records have multiple uses, but some common ones can be to list servers that have the authority to send an email on behalf of the domain (this can help in the battle against spam and spoofed email). They can also be used to verify ownership of the domain name when signing up for third party services.

## Making a Request

1. **Local Cache Check:**
   When you request a domain, your computer first checks its **local DNS cache** to see if the address was recently looked up. If not, it sends the request to a **Recursive DNS Server**.

2. **Recursive DNS Server:**
   Typically provided by your ISP (though you can choose others like Google DNS), this server also checks its **local cache**. If the domain is found (common for popular sites like Google or Facebook), the response is sent back to your computer. If not, the server queries further up the DNS hierarchy.

3. **Root DNS Servers:**
   These servers act as the backbone of the DNS system. They don’t have specific domain information but direct queries to the appropriate **Top-Level Domain (TLD) servers** based on the domain extension. For example, a query for `www.tryhackme.com` would be directed to the `.com` TLD server.

4. **TLD Servers:**
   The TLD server holds information about **authoritative name servers** for domains with that extension. For `tryhackme.com`, the TLD server would direct the query to `kip.ns.cloudflare.com` or `uma.ns.cloudflare.com`.

5. **Authoritative Name Servers:**
   These servers contain the actual **DNS records** (e.g., IP addresses) for the domain. Once the authoritative server responds, the information is sent back to the **Recursive DNS Server**, which caches it for future use, then relays it to your computer.

6. **Caching & TTL:**
   All DNS records come with a **TTL (Time To Live)**, indicating how long the record should be cached before needing to be refreshed. Caching reduces the need for repeated DNS lookups, improving speed and efficiency.
