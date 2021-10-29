# Project 7 - WordPress Pentesting
Time spent: about 8 hours spent in total
> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

###(1) Unauthenticated Genericons Cross-Site Scripting (XSS)
- [ ] Summary: For this Vulnerability by using javascript code, we can trick the user into clicking  specific things either in the comment section or on a post. When this happens, if a script contains code that is malicious, then it can do things that the user wasn't aware of / did not want to do. This was tested in WordPress 4.2, and was fixed in 4.2.2.
- [ ] ![XSS Vuln](https://user-images.githubusercontent.com/73257917/139507040-95762849-7aa0-4225-97a0-94f67e72eaff.gif)


###(2) User Enumeration Vulnerability 
- [ ] Summary: Here I realized that when you enter an incorrect username, the website error give you a hint that the username you enter does not exist. But if you enter a correct username with an incorrect password, then the website just tells you that it's an incorrect passwrod for that username specifically. So that's already a vulnerability in itself but I wanted to show it through burp. I gathered common passwords from the internet and inserted them into burp. When the program finished running, (with a brute-force way) I was able to get the password for that user.(Obviously I knew it was admin, but this still can be misused for wrong intentions). This was tested in Wordpress 4.2.
- [ ] ![Enumeration Vuln](https://user-images.githubusercontent.com/73257917/139507470-5fd145b0-5696-47bf-9180-bfe055bf811f.gif)

##(3) Accessibility Mode Cross-Site Request Forgery (CSRF)
- [ ] Summary: This proved to be a challenge for me, and still not sure if it was correctly done but I still think the way I did it was a vulnerability. Firslty I used the code that was given to us on securty Security Shepherd for one of our CSRF assignments. My objective was to get some infromation from the user by receiving a "POST" request from the user. By hiding this source code into a widget text, I was able to make it so whenever the user wants to go to the main page, they are automatically sent to the log in screen. With this additional infomartion was gathered that was not visible before due to the POST request being processed through burp. This was tested in WordPress 4.2 and was fixed in 4.2.11.
- [ ] ![CSRF Vuln](https://user-images.githubusercontent.com/73257917/139507910-5e63dd8b-aac8-4ad2-a403-3d9e4a9bbcb6.gif)

##(4) Widgets Cross-Site Scripting Vulnerability(XSS)
- [ ] Summary: Once again, with admin access, a person can edit a widget so that it runs a javascript code and either gains information or hinders the user. If the user clicks the "image" icon, they are given a script that in the long run be malicious.
- [ ]  ![XSS Vuln2](https://user-images.githubusercontent.com/73257917/139508224-c779aecd-e3bf-426b-bc47-0d8ccc7a91a7.gif)

## Assets
Script from  Security Shepherd for CSRF.
## Resources
- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)
- Gifs created with ScreenToGif

## Notes
The challenging aspect of this project was how in depth and hard you had to make your work to be. I used the most basic instructions that we learned and tried to re-create those vulnerabilities. Most hints and links from wpscan had used advanced tricks. 
## License

    Copyright [2021] [David Peikrishvili]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
