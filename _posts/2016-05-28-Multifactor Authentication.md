---
layout: post
published: true
title: Multifactor Authentication
comments: true
tags: [Authentication, Information, Security]
---

Looking at the long line up of data breaches with user creditials being dumped on the Internet, it would seem using multifactor authentication for your cloud based services might be a good idea.  Gmail has been using Google Authenticator for quite some time now.  Most cloud based services uses the "something you now" (password) factor.  By adding Google Authenticator you are adding a "something you have" (authenticated smart phone) factor to your authentication process.  The Google Authenticator uses a Time-based One Time Password (TOTP), so the only requirement should be that your smart phone time should be correct.

If you don't have a smart phone or don't want to use it in this way, another interesting device that Gmail integrates with is the [Yubikey](https://www.yubico.com/).  This USB device also integrates with other online services as well as source code management like git ([see setup instructions](https://developers.yubico.com/PGP/Git_signing.html)).  Other interesting uses of the Yubikey is integration with password managers or in applications where a reliable time source may not be available - which would make TOTP unreliable.  

I'm hoping to explore these USB authentication tokens in a bit more detail in future.  
