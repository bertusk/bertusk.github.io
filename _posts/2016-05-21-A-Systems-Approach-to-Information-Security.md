---
layout: post
published: true
title: A Systems Approach to Information Security
comments: true
tags: [Systems, Information, Security]
---

When looking at an Information System there are 3 contact points where users (and attackers) interact with a system.  Any of one or a combination of these contact points can be exploited by an attacker to gain unauthorized access to information.  The 3 contact points includes the hardware, software and management processes for a system.  

Hardware exploits include:

- Hardware level compromises to change a device's functionality 
- Malware that infects a hardware device's firmware (this can be categorized as a software exploit, but I've added it here since it is low enough level to survive an OS re-install like in this case: [How hackers could attack hard drives to create a pervasive backdoor](http://arstechnica.com/information-technology/2015/02/how-hackers-could-attack-hard-drives-to-create-a-pervasive-backdoor/))

Software exploits include:

- Any attack of a software vulnerability like SQL injection, buffer overflow etc.

Management Process exploits include:

- Social engineering attacks that attempt to perform an unauthorized password reset.
- Attempting to get information from backup systems which may not be as well protected as the production system.

![Typical Information System](/assets/InformationSystem.png)
