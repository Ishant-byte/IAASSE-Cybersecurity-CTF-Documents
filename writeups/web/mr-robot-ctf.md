# Mr Robot CTF

- **Platform:** TryHackMe
- **Domain:** Web application security
- **Difficulty:** Medium
- **Status:** Completed (as reported in the source portfolio)

## Objective
Assess a WordPress-based lab, investigate weak administrative authentication, and understand how privileged access to editable server-side code can lead to host compromise.

## Methodology
1. Enumerated the web application and identified WordPress.
2. Used WordPress-focused enumeration and page content to gather contextual clues.
3. Tested the administrative login using a derived wordlist within the lab.
4. Examined how access to the theme editor could permit PHP code execution.
5. Worked through the request path needed to trigger the changed template and then investigated host-level privilege escalation.

## Tools
Nmap, WPScan, Burp Suite, a custom/derived wordlist, and a lab-only reverse-shell payload.

## Findings
Weak administrator credentials enabled dashboard access. The ability to edit server-side theme code created a path to remote code execution in the intentionally vulnerable lab.

## Lessons learned
Getting code into a file is not the same as executing it: understanding the route and request that invokes the file is essential. Defensively, use MFA and strong unique credentials, keep WordPress and plugins updated, restrict file editing in production, apply least privilege, and monitor changes to web files.

## Evidence to add
Add sanitized screenshots of the WordPress identification and the relevant lab result. Do not publish working payloads tied to real hosts or any credentials.
