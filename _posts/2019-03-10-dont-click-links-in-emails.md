---
layout: post
title:  "Do NOT Click Links in Emails... EVER"
author: caveman_actual
tags: [phishing, email-spoofing]
permalink: email-links
---

You never really know who it's from or where it leads to at first glance.  Links can lead to an address other than what is displayed.  For example you may think you are clicking on a
link to a product on Amazon but really to a hacker's machine located at `amaazon.com` where he will
steal your password once you enter it on his site.

### How Are Phishing Campaigns Run
Today there are tools or `kiddie scripts` that allow even non-sophisticated belligerents to spoof
emails and orchestrate phishing and spear-phishing attacks.  Spear phishing implies an attack targeted
at a specific person where phishing is more of a shotgun blast approach hoping to catch anyone willing to fall for the attack.

The first step of running a phishing campaign is to spoof an email that the victim would trust.
Basically this can be done by setting up an email server that allows the attacker to control all the
fields used in the email, most importantly the `To:` and `From:` addresses.  There are open source
products for just about every service[^1] in existence, this makes this process fairly easy for anyone capable of downloading, configuring and hosting a server.  

Once the server is up and running an individual will be targeted in a spear-phishing campaign
or blasted out to a large number of addresses in the general phishing attack.  From here the
attacker needs to create a mock site that makes the victim trust they know where they have landed
after clicking a link in the email.  Really this starts with the faked sender address and message.
If the victim thinks they know who sent the email and the message is convincing enough, the link will
be clicked.  A quick search on the Internet will give many statistics of how many people fall for
phishing attacks.

Once the link is clicked the victim is now interacting with another one of the attackers servers,
most likely an open source web server.  This allows the attacker to create a website that looks like
one the victim may visit often, such as a bank or email provider.  Since this is not really the site
the victim expects, all information entered is given directly to the attacker in plain text; meaning
there is no encryption protecting sensitive information.  This is why a lot of the attacks will look
like pages to reset passwords or enter social security numbers and bank details.

### Real World Example
To show how dangerous these attacks can be I will break down the `Democratic National Committee`
hack of 2016[^2]. The attackers had email addresses of potential victims and knew that they were hosted by Google.  With this information the attackers were able to re-create the reset password dialog screen so
that the victim thought they would be typing their password at a valid location.  Below is an image
of that dialog screen, remember this is not actually a valid site, it is just made to look like
one.  Consider if you thought you received and email from Google would you think this site was legit?

![Google Password Reset Attacker Page](/assets/images/email_links/dnc_hack.png)

The attackers were able to get the victim to this page by using the following URL embedded in the email.
>http://accoounts-google.com/ServiceLoginAuth/i.jsp?continue=https://www.google.com/settings/&followup=https://www.google.com/settings/&docid=Ym9oZGFuLm9yeXNoa2V2aWNoQGdtYWlsLmNvbQ==&refer=Qm9oZGFuK09yeXNoa2V2aWNo&tel=ji8 

Notice `accounts` is spelled `accoounts`, misspelling a single word with a single character is a
common way of tricking a victim.

A common tool used by security researchers is `whois`.  From the tool's manual page...
>The whois utility looks up records in the databases maintained by several Network Information Centers (NICs).

Using that tool with this example we can see that the domain with the attackers URL is no longer
registered, most likely taken down by the attackers or authorities after the successful hack. For
comparison I have run the tool on the valid Google URL below the fake one.

![Whois Lookup Showing Attacker Web Server](/assets/images/email_links/whois_lookup.png)

### Staying Safe
With the above example we can see how convincing some of these attacks have become.  Often the bad actor
will create a sense of urgency with messages like `Your account may be compromised...` which causes
and emotional reaction in the potential victim to act quickly.  There are a few tips that can help
you stay safe in these situations, that you are guaranteed to find yourself in at some point if you use email.

#### Steps to Avoid Becoming a Victim
- NEVER CLICK A LINK IN AN EMAIL
- Navigate to the site via your browser[^3]
- If you get a message to reset your password on Amazon, open your favorite web browser
(Firefox, Chrome, Safari, etc) and type amazon.com in the address bar
- From there navigate to your settings page and change your password this way

- Setup Two Factor Authentication for all accounts that support this feature.  Avoid using another email account or phone number as these can be exploited easily as well.  There are apps such as Authy and Google Authenticator that are safer.  If your password is ever compromised these 2FA apps can help prevent an attacker gaining access to your accounts.

- Also consider choosing an email provider that has efficient Spam filtering.

Following these simple steps will keep you from being re-directed to malicious servers/sites or
downloading malware to your phone or computer.

---

[^1]: When I say service I am talking about the protocols that are necessary for carrying certain types of information across networks. Most of these protocols that we use everyday are based on a client-server architecture. For example let's use searching for `widgets` on Google. When I am on my phone and want to find a `widget` I navigate to _google.com_ and type `widget`. In this example my phone is the _client_ and the computer Google is running on is the _server_.  This is an example of `https` or in general a web service.  There are email services, messaging services, tunnel services and thousands of others.  Splitting network traffic across _services_ allows for more efficient message passing between computers.

[^2]: If you do some research on this event you will likely come across details of 2 separate attacks. The first was in the Summer of 2015 where victims clicked links and downloaded  malware to their computers that allowed the attackers greater levels of access.  This article is focusing on the attack that occurred during the Spring of 2016.

[^3]: A browser is what you use to navigate the web.  The most common ones used are Google's Chrome, Mozilla's Firefox, Apple's Safari and Microsoft's Internet Explorer and Edge.
