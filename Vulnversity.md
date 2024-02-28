# TryHackMe - VULNVERSITY

## Introduction
This repository documents my progress in completing the "VULNVERSITY" room on TryHackMe. The room focuses on various penetration testing and ethical hacking techniques to identify and exploit vulnerabilities in a virtual machine.

## Scan and Enumeration
### Initial Scan
- **Open Ports:** There are 6 open ports on the target machine.

### Squid Proxy Version
- **Squid Proxy Version:** Squid proxy version 3.5.12

### Nmap Scanning
- **Nmap Scanning:** If the flag `-p-400` is used, Nmap will scan 400 ports.

### Operating System Identification
- **Operating System:** Ubuntu

### Web Server Port
- **Web Server Port:** Port 3333

### Nmap Verbose Mode
- **Nmap Verbose Mode Flag:** `-v`

## Web Application Analysis
### Gobuster for Directory Brute-Force
- **Directory with Upload Form:** `/internal/`

### File Upload Form Analysis
- **Blocked File Type:** `.php`

### BurpSuite Fuzzing
- **Allowed Extension:** `.phtml`

## Payload Execution
### Reverse Shell Payload
- **Steps:**
  1. Edited `php-reverse-shell.php` to set the IP to my tun0 IP.
  2. Renamed the file to `php-reverse-shell.phtml`.
  3. Listened for incoming connections using `nc -lvnp 1234`.
  4. Uploaded the shell to `/internal/uploads/php-reverse-shell.phtml`.
  5. Executed the payload by navigating to `http://MACHINE_IP:3333/internal/uploads/php-reverse-shell.phtml`.
  6. Received a connection on the Netcat session.

### Webserver User
- **Webserver User:** `bill`

### User Flag
- **User Flag:** `8bd7992fbe8a6ad22a63361004cfcedb`

## Conclusion
This repository serves as a detailed journal of my experience in completing the "VULNVERSITY" room on TryHackMe. The exercises covered a wide range of penetration testing techniques, enhancing my skills in identifying and exploiting vulnerabilities in a controlled environment.
