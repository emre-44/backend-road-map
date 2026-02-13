# DNS and how it works?

DNS is like the phonebook of the internet. Humans remember names like example.com, but computers understand numbers like `93.184.216.34`. All DNS does is translate the name into the number.

So how does that translation actually happen? The article breaks it down into 5 steps:

1. **Local caches**  
Your computer checks its own memory first. Browser cache, operating system DNS cache, and the hosts file. If you’ve visited the site before, the IP address might already be sitting there.

2. **Recursive DNS resolver**  
If your computer doesn’t know, it forwards the question to a recursive resolver. This is usually your ISP’s DNS server, or a public one like `8.8.8.8`. This server is the persistent one—it won’t give up until it finds an answer.

3. **Root DNS servers**  
The resolver asks a root server. Root servers don’t know the IP either, but they do know one thing: “I don’t handle .com myself, but here’s who does. Go ask them.”

4. **TLD DNS servers**  
These are the servers responsible for `.com, .org, .io`, etc. They also don’t have the final IP address, but they know exactly which authoritative nameserver is in charge of that specific domain.

5. **Authoritative DNS servers**  
This is the actual source of truth. The A record, MX record, everything lives here. It says: “The IP is x.x.x.x.” And the answer travels all the way back down the chain.

The best part of the article is that it doesn’t just explain—it hands you the dig command. Try `dig +trace example.com` and you’ll see all five steps play out in real time. Root → TLD → authoritative → IP. It’s like watching DNS breathe.

It also covers common DNS errors without leaving them as cryptic code:

    NXDOMAIN: The domain doesn’t exist. Typo? Expired?

    NO_INTERNET: The domain exists, but you can’t reach the DNS server. 
     Check your connection.

    BAD_CONFIG: Your DNS settings are misconfigured.

And the classic “flush” trick. When you change DNS settings, your computer stubbornly holds onto the old IP. You can force it to forget:

- Windows: `ipconfig /flushdns`

- Mac: `dscacheutil -flushcache`

If you’re learning about hosting, here’s what DNS means for you:
Your hosting server has an IP address. To point your domain there, you either create an A record (domain → IP) or change the nameservers (domain → your hosting company’s servers). Same job, different door.

**Sources**
- https://cs.fyi/guide/everything-you-need-to-know-about-dns