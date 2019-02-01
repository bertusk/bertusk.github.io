---
layout: post
published: true
title: Off-Path TCP Sequence Number Inference Attack (CVE-2016-5696)
comments: true
tags: [TCP, Off-Path, Linux, Vulnerability, CVE-2016-5696]
---

In the last couple of weeks there has been a lot of articles and discussion on the Off-Path TCP attack.  This attack is made possible by a vulnerability introduced into the Linux TCP stack that leaks information regarding TCP connections.  There has also been a number of articles with ominous sounding titles like "TCP Flaw extends to 80% of android devices".  Even though Android devices are vulnerable, I think these articles are diverting attention away from more likely and more important attack vectors.  The fact that Android devices are vulnerable is somewhat irrelevant for the following reasons:

1. In most Internet communications a client and a server is involved.  This attack can be successful against either the client or the server, so if the server is vulnerable having a non-vulnerable device (like an iPhone) will not protect you.

2. More importantly however, this vulnerability is much easier to exploit against a vulnerable server than a vulnerable client, since clients (Android devices in this case) may not be running any services (I'll explain shortly why this is important).

I will focus on the second point since there is a number of issues around targeting the client side of a TCP connection using this attack.  For any TCP connection there are 4 values that identify the connection.

1. Source IP Address
2. Source Port
3. Destination IP Address
4. Destination Port

For the purposes of this discussion the source IP and port is the client side and the destination IP and port is the server side of the connection.  

The purpose of the attack described in CVE-2016-5696 is to determine if a connection is present between 2 nodes on the internet by discovering these four values (further steps in the attack also attempt to determine the sequence and ack numbers in order to potentially manipulate the connection in some way).  However, this attack can't be used to discover just any random connection.  Since the possible IP address ranges and amount of ports are large, at least 3 of these values must be determined ahead of the attack.  Typically, an attacker could target some server running an application of which the IP address and port number would be known.  At this point the attacker will have to choose a client side IP address.  This may be based on information the attacker obtained through other reconnaissance activities that indicates there is a high likelihood that some client will be connecting to the server on that port.  At this point this vulnerability could help the attacker to determine the client side port and the TCP sequence and ack numbers.  

Based on the [paper](http://www.cs.ucr.edu/~zhiyunq/pub/sec16_TCP_pure_offpath.pdf) describing this attack, the attacker need to send an in-window RST packet to the host (client or server) it is targeting to determine the current ACK throttling counter on that host.  This implies that the attacker has a TCP connection established with the host it is targeting.  A quick nmap scan of my Android phone shows no TCP services available to connect to.  So even though my Android device my have this vulnerability, there is no conceivable way to exploit it using this attack method.  However, I may still be impacted by this type of attack if I connect to a vulnerable server, but the type of device I'm using in such a scenario would be irrelevant.
