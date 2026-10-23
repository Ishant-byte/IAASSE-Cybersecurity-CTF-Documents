# Crack the Hash

- **Platform:** TryHackMe
- **Domain:** Cryptography / password security
- **Difficulty:** Easy

## Objective
Identify password-hash formats and recover the supplied lab passwords using suitable lookup or offline-cracking approaches.

## Methodology
1. Compared hash lengths and format markers to develop candidate algorithm identifications.
2. Used hash-identification utilities to validate likely formats.
3. Checked suitable hashes against an online lookup service where appropriate.
4. Used John the Ripper or hashcat with a wordlist for offline testing when needed.
5. Compared the relative effort required for different hash formats.

## Tools
hashid/hash-identifier, John the Ripper, hashcat, CrackStation, and rockyou.txt.

## Findings
The room illustrated that weak passwords may be recoverable from common wordlists, while hash algorithms differ substantially in resistance to guessing. In the source notes, the bcrypt example took longer to crack than the sha512crypt example under the tested conditions.

## Lessons learned
Hash format and work factor strongly affect guessing cost. For real systems, use a modern password-hashing scheme such as Argon2id (or an appropriately configured bcrypt/scrypt/PBKDF2 deployment), unique salts, and strong passwords. Avoid submitting private or real user hashes to third-party lookup sites without authorization.

## Evidence to add
Use redacted screenshots showing hash identification and tool settings, not plaintext passwords or flags.
