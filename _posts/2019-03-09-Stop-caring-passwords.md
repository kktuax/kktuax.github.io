---
layout: post
title: "How I stopped caring about passwords once and for all"
tags: [password, lesspass]
---

Not so long ago we heard news about huge password breaches like [Collection #1](https://mashable.com/article/collection-1-password-breach). The scale is quite concerning but this type of password breaches sadly happen quite often. There are even sites like [have i been pwned?](https://haveibeenpwned.com/) where you can find out how many times your passwords have been leaked.

*Should I be concerned?* Well, probably yes, unless you have been following a [strict password policy](https://security.web.cern.ch/security/recommendations/en/passwords.shtml) since you signed up on some web site for the first time, someone else could have gained access to your online accounts. Specially if you have shared credentials between several services, you should be taking some action.

## Password managers

The first logic approach should be to use a different password per account but, without the help of a tool to store all this information, it can become really hard to remember all of them. There are a [lot of tools](https://en.wikipedia.org/wiki/List_of_password_managers) than can help with with this matter. However, they normally keep your passwords (sometimes even stored in plaintext) in your machine, which in case of someone gaining access to them, could be potentially dangerous.

There is another problem when you want to have access to your passwords from multiple devices (home/work PC, mobile, tablet, etc). This requires a sync process with your passwords which can be again a security risk. Also your took of choice should be available in all platforms which sometimes can be hard to achieve.

## Use an algorithm, not a tool

![lesspass logo]({{ "/assets/img/lesspass.png" | relative_url }})

One day of busy procrastination I found [lesspass](https://lesspass.com), which follows a different approach: you generate a unique password per site, out of a master password (which is not stored), and a bunch of non private information (e.g. site name and login). Since this is an algorithm you can run it from any machine, or even directly from [the web page](https://lesspass.com). You can self host it if you are a bit more paranoid, but since they only keep a list of sites and public information, I'm confortable using just the web page.

![lesspass logo]({{ "/assets/img/lesspass-login.png" | relative_url }})

Using the default configuration you will generate passwords with a fixed length and mixing letters and special characters, something like `eF_(<]ad^{1S4$Ao`, but if can be configured to generate other types of passwords: using different lengths, or with certain types of characters. This can come handy in cases where they impose some ~~stupid~~ rules about how passwords should look like, for instance in the typical e-banking sites. 
