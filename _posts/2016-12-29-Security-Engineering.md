---
layout: post
published: true
title: Security Engineering
comments: true
tags: [Security, Engineering, Books, Reading]
---

In the last while I've had some people ask me about getting into the field of Information Security and the related certifications.  This is a difficult question to answer since the field of Information Security is large with many areas of specialization.  Not all the areas of specialization are technical either.  In this post I would like to focus on the area of Security Engineering which has a more technical focus and leans more towards the research and development side of Information Security rather than the managment, compliance or operational side.  There are several good blog posts about getting into Security Engineering.  One which I found really helpful is: [Getting Into Security Engineering](https://noncombatant.org/2016/06/20/get-into-security-engineering/). This blog post by Chris Palmer provides a fairly extensive reading list on topics fundamental to Security Engineering.  These topics can be organized in 4 broad knowledge areas.

### 1. Programming and low level programming concepts
This area not only covers high level programming and scripting for exploit and testing purposes, but also knowledge of lower level concepts of how machine instructions are loaded and executed and how it may cause buffer overflows and other similar vulnerabilities.  This knowledge area also covers topics related to secure software development concepts.

### 2. Platform and OS concepts
This area covers knowledge of operating systems including system administration, security mechanisms in the OS, process isolation etc. In depth knowledge of at least 1 operating system be it Linux, Mac OS, Windows or a Mobile OS of some kind is highly desirable.

### 3. Networking
This knowledge area covers networking of any kind (wired, wireless etc.).  Knowledge of TCP/IP is crucial for any Security Engineer.

### 4. Cryptography
This knowledge area covers all facets of keeping information confidential.  Knowledge of symmetric and asymmetric key encryption, hashing and digital signatures are fundamental knowledge areas.

## Building Skills
There are definitely overlap in these knowledge areas since system administration more often than not include the network configuration of a server and the network stack is implemented in software which may be susceptible to vulnerabilities like buffer overflows etc.  Most operating systems and some network protocols also makes use of some form of cryptography.  So building skills in all these knowledge areas will create a more complete picture of Security Engineering.

As part of my transition into Security Engineering I'm currently exploring the reading list recommended in Chris' blog post.  I included the following on my reading list from Chris' blog post.  There seem to be a lack of book recommendations in the Platform and Operating System area, so I might have to do a bit more research into good resources in this space.  As time permits, I'll post some book reviews.

### Reading List

| Book  | Author  | Knowledge Area |
|---|---|---|
| The Hitchhiker's Guide To Python | Kenneth Reitz | Programming |
| Silence On The Wire | Michal Zalewski | Programming, Networking |
| The Tangled Web | Michal Zalewski | Programming, Networking |
| Cryptography Engineering | Ferguson, Schneier, and Kohno | Cryptography |
| TCP/IP Illustrated, Volume 1: The Protocols | W. Richard Stevens | Networking |
| Art of Assembly Language | Randall Hyde | Programming |
| Security Engineering | Ross Anderson | General |
| The Art Of Software Security Assessment | Dowd, McDonald, and Schuh | Programming |
