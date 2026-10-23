# Bounty Hacker

- **Platform:** TryHackMe
- **Domain:** Network security
- **Difficulty:** Easy

## Objective
Use service enumeration and an exposed FTP resource to understand a credential compromise path, then investigate a local privilege-escalation misconfiguration.

## Methodology
1. Scanned the lab and identified FTP, SSH, and HTTP services.
2. Tested the permitted anonymous FTP access and reviewed the files exposed by the share.
3. Retrieved a task-list file and a password-list-style file from the lab share.
4. Used the provided context to test SSH authentication in the lab.
5. Enumerated local privileges and identified a sudo configuration issue.

## Tools
Nmap, FTP client, Hydra, SSH, and `sudo -l`.

## Findings
Anonymous FTP exposed files that helped with credential discovery. A sudo misconfiguration then provided a path to elevated privileges in the lab.

## Lessons learned
The FTP directory listing initially stalled because of passive-mode behavior; changing the client mode resolved the issue. Privilege escalation should be based on carefully checking the actual sudo permissions rather than assumptions. Defensively, disable anonymous FTP unless needed, restrict exposed files, use strong SSH authentication, and audit sudoers rules.

