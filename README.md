# Project 7 - WordPress Pentesting
Time spent: about 8 hours spent in total
> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

###(1) Unauthenticated Genericons Cross-Site Scripting (XSS)
- [ ] Summary: For this Vulnerability by using javascript code, we can trick the user into clicking  specific things either in the comment section or on a post. When this happens, if a script contains code that is malicious, then it can do things that the user wasn't aware of / did not want to do. This was tested in WordPress 4.1-4.2.1, and was fixed in 4.2.2.
