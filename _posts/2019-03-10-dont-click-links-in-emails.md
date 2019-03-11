---
layout: post
title:  "Do NOT Click Links in Emails... EVER"
author: caveman_actual
tags: [phishing, email-spoofing]
permalink: email-links
---

You never really know who it's from or where it leads to at first glance.  Links can point to
addresses that are not what they are displayed as.  For example you may think you are clicking on a
link to a product on Amazon but really to a hacker's machine located at amaazon.com where he will
steal your password once you enter it on his site.

### How Are Phishing Campaigns Run
Today there are tools or `kiddie scripts` that allow even non-sophisticated belligerents to spoof
emails and orchestrate phishing and spear-phishing attacks.  Spear phishing implies a targeted
attack where phishing is more of a shotgun blast approach hoping to catch anyone willing to fall for
the attack.

The first step of running a phishing campaign is to spoof an email that the victim would trust.
Basically this can be done by setting up an email server that allows the attacker to control all the
fields used in the email, most importantly the `To:` and `From:` addresses.  There are open source
products for just about every service in existance you can run a server for, this makes this process
fairly easy for anyone capable of downloading, configuring and hosting the server.

Once the server is up and running than an individual will be targeted in a spear-phishing campaign
or blasted out to a large number of addresses in the general phishing attack.  From here the
attacker needs to create a mock site that makes the victim trust they know where they have landed
after clicking a link in the email.  Really this starts with the faked sender address and message.
If the victim thinks they know who sent the email and the message is convincing enough the link will
be clicked.  A quick search on the internet will give many statistics of how many people fall for
phishing attacks.

Once the link is clicked the victim is now interacting with another one of the attackers servers,
most likely an open source web server.  This allows the attacker to create a website that looks like
one the victim may visit often, such as a bank or email provider.  Since this is not really the site
the victim expects, all information entered is given directly to the attacker in plain text; meaning
there is no encryption protecting sensitive information.  This is why a lot of the attacks will look
like pages to reset passwords or enter social security numbers and bank details.

### Real World Example
To show how dangerous these attacks can be I will break down the `Democratic National Committee`
hack of 2016. (If you do some personal research on this event you will likely come across details of
2 seperate attacks.  The first was in the Summer of 2015 where victims clicked links and downloaded 
malware to their computers that allowed the attackers greater levels of access.  This article is 
focusing on the attack that occurred during the Spring of 2016.) 

![Whois Lookup Showing Attacker Web Server](/assets/images/email_links/whois_lookup.png)
![Google Password Reset Attacker Page](/assets/images/email_links/dnc_hack.png)
