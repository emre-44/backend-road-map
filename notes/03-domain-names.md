# What is Domain Name?

## What is a Domain Name? A Detailed Breakdown

Imagine trying to visit a friend's house, but instead of a street address, you only had the exact latitude and longitude coordinates. You *could* use them, but it would be a huge hassle. That's essentially what the internet was like before domain names.

At its core, a **domain name** is your website's human-friendly street address. It's the text you type into a browser, like `google.com` or `amazon.co.uk`. Computers, however, locate websites using numerical Internet Protocol (IP) addresses, which are long strings of numbers like `192.0.2.2`.

The magic that connects the easy-to-remember domain name to the hard-to-remember IP address is the **Domain Name System (DNS)** . Think of DNS as the internet's phonebook. When you type a domain name, a DNS lookup happens instantly in the background, translating that name into the correct IP address so your browser can load the site.

## Domain Name vs. URL: Not the Same Thing

People often use these terms interchangeably, but they are different. A **URL (Uniform Resource Locator)** is the full web address for a specific page. The domain name is actually just one part of the URL.

Example: In the URL `https://www.cloudflare.com/learning/`, the part **cloudflare.com** is the domain name. The https is the protocol, and **/learning/** is the specific path to a page on that site.

## The Anatomy of a Domain Name

Domain names are structured in a hierarchy, read from right to left, moving from the most general to the most specific category.

    Top-Level Domain (TLD): This is the most general part, found to the right of the last dot.  
    It includes generic TLDs (gTLDs) like .com, .org, .net, and country-code TLDs (ccTLDs) like .uk, .jp, or .tr.

    Second-Level Domain (2LD): This is the unique, descriptive name you choose,  
    located directly to the left of the TLD. In google.com, the word 'google' is the second-level domain.  

    Third-Level Domain (3LD) or Subdomain: Sometimes, an additional part is added to the left of the 2LD. 
    For instance, in google.co.uk, the 'co' indicates a company (this is the 2LD in a ccTLD structure), 
    and 'google' is actually the third-level domain. The 'www' you often see is also a common subdomain (e.g., www.).  

## How to Get and Keep a Domain Name

You can't buy a domain name forever; you lease it for a period of time through a **domain registrar** (like Cloudflare Registrar, GoDaddy, etc.). These registrars work with central domain registries to reserve the name for you.

Here are some critical things to know about managing them:

    Domain Security & Registrars: Choosing an honest registrar is vital. Unethical ones 
    may let your domain expire and immediately buy it to sell it back to you at a huge profit.

    Domain Squatting: This is the bad-faith practice of registering a domain name 
    you intend to resell to the rightful trademark owner or use for malicious purposes.

    Domain Privacy: When you register a domain, your contact info is typically public in the WHOIS database.
    Domain privacy services conceal this info to protect you from spam and harassment.

    Premium & Expired Domains: Some domains are considered "premium" and cost much more due to their 
    high marketing value or simplicity. When a domain expires, it can be renewed, auctioned off, or become a target for squatters.

In short, a domain name is the cornerstone of your online identity. It’s a simple concept powered by a complex global system (DNS), and choosing a good registrar is your first and most important step in protecting that identity.

**Sources:**  
- https://www.cloudflare.com/en-gb/learning/dns/glossary/what-is-a-domain-name/ 
