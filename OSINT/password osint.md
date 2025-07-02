
markdown
Copy
Edit
# 🔐 Password OSINT — Gathering Password Intelligence from Open Sources

Password OSINT refers to using **open-source tools and techniques** to discover or analyze passwords or password patterns without hacking. It focuses on publicly available data like breaches, reused credentials, metadata, and behavior clues.

---

## 🧠 Use Cases

Used in:
- Red Teaming
- Penetration Testing
- Social Engineering
- Threat Intelligence & Reconnaissance

---

## 🧰 Common Password OSINT Techniques

### 1. 🧾 Breached Database Lookups (Credential Leaks)
Identify leaked usernames/emails and passwords from past breaches.

**Tools & Platforms:**
- [HaveIBeenPwned](https://haveibeenpwned.com)
- [Dehashed](https://www.dehashed.com) *(paid)*
- [Scylla.sh](https://scylla.sh)
- Breach-Parse, Snusbase, LeakCheck.io

**Example:**
```bash
holehe email@example.com
Checks if the email is linked to breached accounts.

2. 🧠 Password Reuse Pattern Recognition
Most users reuse or slightly alter passwords:

nginx
Copy
Edit
password123 → Password123! → Password1232024
Tool:

CUPP (Common User Passwords Profiler)

bash
Copy
Edit
python3 cupp.py -i
3. 📄 PDF/Document Metadata
Extract possible passwords or hints from embedded metadata.

Tools:

bash
Copy
Edit
strings file.pdf
exiftool file.docx
4. 🧰 GitHub OSINT (Password Leaks in Public Repos)
Developers accidentally commit secrets like:

.env files

config.js

API keys

Database credentials

Tools:

GitHub Dorks

bash
Copy
Edit
filename:.env password
GitLeaks

TruffleHog

5. 🧑‍💼 Social Media & Behavioral Clues
People often use personal info in passwords like:

Pet names

Birthdates

Favorite teams/movies

Sources:

Facebook/Instagram bios

TikTok Q&A

GitHub commits

Wordlist Generation Tools:

Mentalist

Cewl

bash
Copy
Edit
cewl http://target.com -w wordlist.txt
6. 🌐 Paste Sites & Dark Web Dumps
Monitor paste dumps that may contain exposed passwords.

Platforms:

Pastebin

Ghostbin

Tools:

PasteHunter

LeakLooker

Onyphe.io

7. 📡 Shodan + Weak Login Detection
Search for exposed services with default credentials:

vbnet
Copy
Edit
title:"Login" default password
"Server: MikroTik"
Targets:

Admin Panels

CCTV

IoT Devices (e.g., routers, webcams)

Tools:

Shodan

ZoomEye

⚠️ Ethics & Legal Disclaimer
Use Password OSINT only for legal and ethical purposes, such as:

Security research

Bug bounty

Educational exercises

Authorized red teaming

Never use this information for:
❌ Illegal access
❌ Unauthorized probing
❌ Harassment or exploitation

✅ Summary Table
Technique	Description	Tools/Examples
Breach Lookups	Find leaked credentials	HaveIBeenPwned, Dehashed, holehe
GitHub Secrets	Search public repos for committed secrets	GitHub dorks, GitLeaks, TruffleHog
Password Profiling	Generate passwords based on user traits	Cupp, Cewl, Mentalist
Metadata Scanning	Look inside files for embedded data	exiftool, strings
Default Credential Search	Identify exposed systems with weak creds	Shodan, ZoomEye
Social Media Clues	Extract user info used in passwords	Facebook, Instagram, TikTok
Dark Web Dumps	Watch for leaks in pastebin/darknet	Pastebin, PasteHunter, Scylla

Want a Python script or toolset to automate this recon workflow? Ask to generate one!

yaml
Copy
Edit

---
