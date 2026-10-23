# GoldenEye

- **Platform:** TryHackMe
- **Domain:** Network security
- **Difficulty:** Medium

## Objective
Investigate a themed Linux lab with a webmail interface and POP3 service, then follow discovered evidence to obtain access and complete the privilege-escalation path.

## Methodology
1. Used Nmap to identify the HTTP/webmail and POP3 services.
2. Reviewed contextual clues to narrow the candidate usernames, including Boris.
3. Tested the identified mailbox with Hydra in the authorized lab environment.
4. Diagnosed repeated POP3 disconnections and adjusted execution timing/parallelism.
5. Reviewed mailbox messages for additional credentials and clues.
6. Used the recovered information to establish a foothold, obtain an interactive shell, and investigate local privilege-escalation paths.

## Tools
Nmap, Hydra, a POP3 client, Python, and Linux privilege-escalation enumeration tools.

## Findings
The lab demonstrated how a weak mailbox password and sensitive information stored in email can create a chain of compromise. The main obstacle was the POP3 service disconnecting during authentication attempts; tuning the testing approach helped progress past the issue.

## Lessons learned
Service behavior matters: blindly increasing concurrency can make a fragile service less reliable. Record errors, change one parameter at a time, and verify each result. In production, use strong unique passwords, MFA where supported, login throttling, alerting, and avoid storing reusable credentials in mailboxes.
