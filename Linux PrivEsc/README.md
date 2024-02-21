# Mastering Linux Privilege Escalation🚀

## Introduction
Hey fellow hackers and cybersecurity enthusiasts! 👋 
TryHackMe's Linux Privilege Escalation room, a medium-difficulty challenge that took me on an insightful journey through various techniques.

## 1. Weak File Permissions
I kicked off by exploiting weak file permissions. After saving the root user's hash to a file called `hash.txt`, I utilized John the Ripper to crack it successfully. Switching to the root user, I created a new password using `openssl passwd` and updated the root user's credentials.

## 2. GTFOBins Exploration
The exploration of [GTFOBins](https://gtfobins.github.io) was eye-opening. I delved into sudo privileges and learned how to escalate my privileges using escape sequences. This part was crucial for understanding advanced privilege escalation techniques.

## 3. Shell Feature Abuse
Abusing shell features became an integral part of my strategy. Understanding how to manipulate shell functionalities allowed me to escalate privileges efficiently in various scenarios.

## 4. Passwords & Keys - History Files
The exploration of history files proved fruitful. I uncovered how a user's mistyped password on the command line can end up in history files, presenting a potential security risk. Additionally, config files often held plaintext passwords and other sensitive information.

## 5. Kernel Exploits
Venturing into kernel exploits was both thrilling and cautionary. I utilized the Linux Exploit Suggester 2 tool to identify potential vulnerabilities on the current system, with a particular focus on the notorious Dirty COW exploit.

## 6. Privilege Escalation Scripts
Running privilege escalation scripts added a layer of automation to my toolkit. The Linux Exploit Suggester 2 tool and other scripts proved invaluable in identifying and exploiting potential weaknesses in the system.


Happy hacking!
