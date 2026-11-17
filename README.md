# Week 3 - Project Module 1: Password Cracking with John the Ripper (JTR)

## Overview
In this lab, I acted as a penetration tester performing offline password cracking using **John the Ripper (JTR)** on Kali Linux. The objective was to identify hash types, run wordlist and rule-based attacks against captured hashes, and recover the target password (the flag) — demonstrating why weak passwords and unsalted hashes are a critical risk.

## Lab Environment
* **Attacker Machine:** Kali Linux
* **Tool:** John the Ripper (JTR)
* **Wordlist:** rockyou.txt (`/usr/share/wordlists/rockyou.txt`)
* **Attack Type:** Offline dictionary + rule-based cracking

## Tasks Performed

### Task 1: Identify the Hash Type
* Extracted the hash from the provided file.
* Used `hash-identifier` / JTR's auto-detection to determine the hash algorithm before attacking.

### Task 2: Prepare the Wordlist
* Decompressed the built-in rockyou wordlist:
```bash
sudo gunzip /usr/share/wordlists/rockyou.txt.gz
