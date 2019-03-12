---
layout: post
title:  "What Is DNS and Why Should I Care"
author: caveman_actual
tags: [dns]
permalink: what-is-dns
---

Domain Name System/Server (DNS) is basically what a phone book used to be.  Not too long ago when a person needed a plumber she may go to the _YellowPages_ book stored in a kitchen drawer and look up the phone number for _AAA Plumbers_.  Today when you type `www.instagram.com` in a browser your computer, nor any other for that matter knows what you're talking about.  DNS will tell your computer what IP Address will take you to the closest InstaGram server.


### Why Should I Care

Just as the phone book could translate a business name to a phone number, a DNS server will translate a URL to an IP Address.  The IP Address is used to direct your requests across the Internet to the destination you need to get the information you are looking for, whether it be search results from Google or posts from Facebook.  Without DNS you wouldn't be able to access any of this information.

Why does that matter for the layman... it kind of doesn't, but later posts will discuss VPNs[^1] and how to protect yourself while on public networks or hide traffic from your service provider while at home.  Understanding DNS is important in this context because it happens before you can start communicating with websites over HTTPS[^2].  To help explain what is happening please refer to the image below.

![DNS](/assets/images/dns/dns.png)
<sub>Steps of what happens when a user wants to view some content on any of the popular sites shown.</sub>

1. For this example let us say we want to go to `LinkedIn`.  The first step to to make a DNS request that is handled by the DNS server.
1. The DNS server responds to our request for the IP Address for the closest `LinkedIn` server, i.e. `108.174.10.10`.
1. The user's browser now knows that `www.linkedin.com` is located at `108.174.10.10` and we can start interacting with the site.


### What Does this Have to Do with a VPN

Most users will invest in a VPN to protect themselves from being hacked while on a public network like in an airport, coffee shop or hotel.  If it is not configured properly you can still expose yourself to DNS attacks.  Understanding that DNS is different than HTTPS is the first step in making sure your VPN is as robust as possible.

---

[^1]: Virtualized Private Network, primarily used to wrap any information you are sending over a network in an encrypted tunnel.

[^2]: HTTPS is the main way of moving web traffic around the Internet.  HTTP stands for Hyper Text Transfer Protocol and the S stands for secure.  The current security protocol is TLS which recently replaced SSL.
