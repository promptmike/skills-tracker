# DNS in Detail

## Task 1 - What is DNS?

Domain Name System (DNS) allows us to access devices remotely without remembering their IP Addresses.
DNS makes it possible to visit a website with its URL so you don't need to remember the IP Address of the server.

## Task 2 - Domain Hierarchy

### Domain Hierarchy

#### TLD (Top-Level Domain)

Generic Top Level Domains (gTLD) tell us the purpose of a site, while Country Code Top Level Domains (ccTLD) tell us geographic location.
The right-hand part of a Domain Name is the TLD, which can be Generic or Country Code.

#### Second-Level Domain

The Second Level Domain is limited to 63 characters of a-z, 0-9 and hyphens, but cannot start or end with a hyphen or have consecutive hyphens.
TLD goes on the right to tell us purpose or location, SLD comes before .tld and must meet strict character requirements.

#### Subdomain

Subdomains have the same restrictions as SLD, but you can have multiple Subdomains provided the total length is 253 characters or less.
TLD goes on the right, SLD before it and Subdomain or multiple Subdomains before SLD.

## Task 3 - Record Types

### DNS Record Types

There are many types of DNS Record, not just for websites.
For a website, TLD goes on the right, SLD before it (63 characters or less) and Subdomains before SLD (63 characters each, 253 total).

#### A Record

An A Record resolves to an IPv4 Address.
There are many types of DNS Record, such as A Record that resolves to an IPv4 Address.

#### AAAA Record

A AAAA Record resolves to an IPv6 Address.
There are many types of DNS Record, such as A Record that resolves to IPv4 and AAAA Record that resolves to IPv6.

#### CNAME Record

CNAME Record resolve to another Domain Name (e.g. for redirecting a Subdomain to another site for e-commerce).
There are many types of DNS Record, such as A Record that resolves to IPv4 and AAAA Record that resolves to IPv6.

#### MX Record

MX Records resolve to the email servers for the Domain queried, with priority flag to show which order to try the servers (you can have backups).
There are many types of DNS Record, such as A Record for IPv4, AAAA Record for IPv6, CNAME Record for redirect and MX Record for email.

#### TXT Record

TXT Records are free text fields for additional data. Often used to list authorised email servers or to verify Domain ownership.
A Records resolve to IPv4, AAAA records to IPv6, CNAME Records to another Domain, MX Records to email servers and TXT Records to additional text.

## Task 4 - Making A Request

### What happens when you make a DNS request

First your computer checks its own cache, then if it has no local record it sends a request to your Recursive DNS Server.
DNS Records come in many types and can be stored in cache for frequent use, else they must be obtained from a DNS Server.

A Recursive DNS Server, usually the one provided by your ISP, keeps a large cache of DNS Records it can return in response to requests.
DNS Records come in many types and can be stored in cache for frenquent use or obtained from a DNS Server.

If the Recursive Server does not have the DNS Record you need, it will redirect you to a Root DNS Server which redirects you to a TLD DNS Server.
DNS Records come in many types and are stored in local cache, Recursive DNS Server cache redirected to by TLD DNS Servers.

The TLD DNS Server holds records of the authoritative servers (Nameservers) for each SLD in its TLD.
DNS Records come in many types and are stored in local cache and Recursive DNS Server cache for frequent use or redirected to by TLD DNS Servers.

Nameservers store the DNS Records for a particular domain, while the Recursive DNS Servers cache the DNS Records you request with a TTL.
Nameservers store the DNS Records for a particular Domain, TLD DNS Servers redirect to Nameservers and Recursive DNS Server cache the DNS Records.

# Task 5 - Practical

Build requests to make DNS queries.
Nameservers answer requests for DNS Records, TLD Servers redirect to the correct Nameservers and Recursive Servers cache the records.