# Domains & DNS

The Internet is a distributed system of interconnected computers throughout the world.

Each computer as an address, know as an IP Address, but mostly humans want something more memorable—that’s where domains come in.

### [☛ Videos for domains]()

---

- [Domains & IPs](#domains--ips)
- [How everything connects together](#how-everything-connects-together)
	- [How you see a website](#how-you-see-a-website)
	- [How e-mails are sent](#how-e-mails-are-sent)
- [Links & resources](#links-and-resources)

---

## Domains & IPs

Domains, like `google.com` or `algonquindesign.ca`, are just for humans so we can more easily remember where a website is.

But computers don’t necessarily care about domains, they care about IP address, which are the actual locations/names of the computers connected to The Internet. *Every single computer connected to the Internet has a unique IP address.*

An IP address looks something like this: `192.168.1.0` or `2001:0db8:85a3:0000:0000:8a2e:0370:7334`—which aren’t terribly memorable for regular mortals. Whereas, domains like `github.com` are much more memorable.

So the purpose of the Domain Name System (DNS) is to map domains to IP address and provide other information about a website.

A simple example of DNS records might look like this:

```
algonquindesign.ca.        A    192.168.0.1
mail.algonquindesign.ca.   MX   192.168.0.2
```

There’s a direct connection between a domain and it’s associated IP address.

---

## How everything connects together

![](domains-dns-servers.png)

### How you see a website

After you type the domain into your browser and go your computer starts making a bunch of really quick requests (less than 100 ms):

1. Your computer connects to a DNS server, requesting DNS information for the domain you typed in.
	Your computer already knows the IP address to at least one DNS server because your Internet provider sent it to your computer.
2. The DNS will then send back the IP address of the computer that hosts the website to your computer, if it knows it.
	If it doesn’t know the IP address it will send your computer the IP address of another name server that might know.
	The loop continues until your computer has the IP address of the host.
	**IP address of the website host is called the `A` record.**
3. When your computer gets the IP address it connects directly to the host computer and requests to see the website.
4. The host/web-server will then return the `index.html` file for the website you requested.
	Your browser will then start requesting all the other resources of your website like CSS, images, Javascript, etc.
	If those resources are located on another domain the whole process starts all over again at step 1.

**Authoritative name server**

The `NS` records in your DNS information points to the primary name server for your domain—usually your registrar.

All the domain servers synchronize with each other so it can take time for your domain records to show up on all the DNS servers around the world.

If the DNS server your browser requests doesn’t know the IP for the domain you want, or if that information has expired, your computer will most likely connect to the authoritative name server for your domain to get the real, fresh DNS information.

### How e-mails are sent

The process for sending e-mails is similar to viewing a website but requires more requests and more DNS records.

**The DNS records for e-mail servers are called the `MX` records.**

After you write your e-mail message and click send a whole bunch of requests are sent out again:

1. Your computer connects to a DNS to find the `A` record for your mail server.
2. The DNS sends back the IP for your e-mail server.
3. Your computer connects to your e-mail server using the new IP and submits a new message.
4. Your e-mail server then connects to the DNS to find the `MX` record for the domain of the person you’re sending your message to.
5. The `MX` record is sent back to your computer.
6. If the `MX` record isn’t an IP address a whole new DNS lookup must happen for the `A` record of the other mail server.
7. The DNS will then send back the IP address of the other person’s e-mail server.
8. Your e-mail server connects to the other person’s e-mail server and posts the new message on it.

---

## Links and resources

**DNS tools**

- [MX Toolbox](http://mxtoolbox.com/)
- [Pingdom: DNS check tool](http://dnscheck.pingdom.com/)

**Recommended registrars**

- [Hover](https://www.hover.com/)
- [Gandi](http://www.gandi.net/)

**Recommended e-mail providers**

- [FastMail](https://www.fastmail.com/)

**Recommended website hosts**

- [GitHub](https://github.com/)
- [WiredTree](https://www.wiredtree.com/)
- [A Small Orange](http://asmallorange.com/)
- [SiteGround](http://www.siteground.com/)
- [DreamHost](https://www.dreamhost.com/)

**Security & performance**

- [CloudFlare](https://www.cloudflare.com/)
