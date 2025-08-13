# Pre-Security - DNS in Detail

## 🧠 What I learned

### Task 1 - What is DNS?
- aka Domain Name System
- Provides a simple way to communicate with devices on the internet using words instead of IP Address
- human readable
- e.g. instead of going to 104.26.10.229, you can go to tryhackme.com

### Task 2 - Domain Hierarchy
- TLD (or Top-Level Domain)
  - e.g. .com .biz .co.uk
  1. gTLD (or Generic Top-Level Domain)
    - .com .biz .org .edu .gov
    - used to tell domain name's purpose
  2. ccTLD (or Country Code Top Level Domain)
    - e.g. .ca for Canada, .co.uk for United Kingdom

- Second-Level Domain
  - in tryhackme.com > tryhackme is the second-level domain
  - limited to 63 characters + TLD
  - only use a-z 0-9 and hyphens

- Subdomain
  - is on the left-hand side of second level domain
  - uses period to separate it from second level domain
  - in www.tryhackme.com > www is the subdomain
  - also 63 characters only and a-z 0-9
  - can also be jupiter.servers.tryhackme.com
    - but length must be kept to 253 characters or less
  - no limit to number of subdomains

### Task 3 - Record Types
- DNS is not only for websites
- can also be for email such as MX record
  - A Record
    - resolve to IPv4 addresses
  - AAAA Record
    - resolve to IPv6 addresses
  - CNAME Record
    - resolve to another domain name
    - e.g. store.tryhackme.com returns shops.shopify.com
    - another DNS request would be made to to shops.shopify.com to get the actual IP Address
  - MX Record
    - resolve to the address of servers handling the email for the domain being queried
  - TXT Record
    - free text fields where text-based data can be stored
    - common use is to list servers that have authority to send an email on behalf of the domain which is used to battle against spam and spoof email
    - verify domain ownership

### Task 4 - Making a request
- What happens when one make a DNS request (or go to a website such as google.com)
  1. Computer first checks its local cache for the IP Address if previous lookup has been done
  2. If not found, computer checks the recursive DNS resolver and it will check its own cache for the IP Address
  3. If still not found, the recursive resolver will ask the root server where to find the TLD for the domain. e.g. www.tryhackme.com > rooter server will respond with the address of .com TLD server
  4. The recursive resolver will ask the .com TLD server to find the authoritative DNS server for tryhackme.com
  5. The recursive DNS resolver will send request to the authoritative DNS server for the IP Address
  6. The recursive resolver will send IP Address to the computer, and local copy will be cached to computer (local cache) and recursive DNS resolver

### Task 5 - Practical
- Used the provided local cache and typed in:
  - nslookup --type=CNAME shop.website.thm
  - nslookup --type=TXT website.thm
  - nslookup --type=MX website.thm
  - nsloopup --type=A website.thm