# 🕵️ OSINT Field Guide & Toolkit

Welcome to the **Open Source Intelligence (OSINT) Toolkit** — a structured collection of concepts, tools, and examples for discovering publicly available information such as usernames, emails, phone numbers, locations, and other digital footprints without hacking or breaking the law.

This guide is designed for ethical hackers, cybersecurity analysts, red teamers, investigators, and OSINT hobbyists.

---

## 📘 What is OSINT?

**OSINT (Open-Source Intelligence)** is the process of gathering, analyzing, and using publicly accessible information to produce actionable intelligence. This includes:
- Internet content (social media, blogs, forums)
- Government databases
- Public records
- Multimedia files (images, videos, documents)

OSINT is used in cybersecurity, journalism, law enforcement, penetration testing, corporate investigations, and even warfare.

---

## 📚 Table of Contents

1. [Footprinting vs Fingerprinting](#1-footprinting-vs-fingerprinting)
2. [Image Reversing & EXIF Metadata](#2-image-reversing--exif-metadata)
3. [Geolocation OSINT](#3-geolocation-osint)
4. [GeoGuessr (Gamified OSINT)](#4-geoguessr-gamified-osint)
5. [Creepiest OSINT Examples](#5-creepiest-osint-examples)
6. [Discovering Email Addresses](#6-discovering-email-addresses)
7. [Password OSINT](#7-password-osint)
8. [Hunting Usernames & Passwords](#8-hunting-usernames--passwords)
9. [Searching for People](#9-searching-for-people)
10. [Vector Records in OSINT](#10-vector-records-in-osint)
11. [Hunting Phone Numbers](#11-hunting-phone-numbers)
12. [Ethical Warning](#12-ethical-warning)

---

## 1. Footprinting vs Fingerprinting

### 📌 Concept:
These are **reconnaissance techniques** used in the early stages of ethical hacking or OSINT research.

| Term | Description | Example |
|------|-------------|---------|
| **Footprinting** | Passive data collection from public sources | WHOIS lookup on domain |
| **Fingerprinting** | Actively interacting with systems to gather data | Scanning ports with Nmap |

### 🔧 Tools:
- WHOIS, nslookup, theHarvester (for footprinting)
- Nmap, Netcat, Wappalyzer (for fingerprinting)

---

## 2. Image Reversing & EXIF Metadata

### 🖼️ Concept:
Images can contain hidden or contextual data used for identifying origin, location, or authorship.

- **Image Reversing**: Finding the source or similar copies of an image
- **EXIF Metadata**: Hidden data in image files (e.g., GPS, camera info)

### 🔧 Tools:
- `exiftool` – Extracts image metadata
- [Yandex Images](https://yandex.com/images) – Best for facial search
- [Google Images](https://images.google.com) – Reverse search for websites
- [InVID Plugin](https://www.invid-project.eu/tools/invid-plugin/) – Video verification

---

## 3. Geolocation OSINT

### 📍 Concept:
Identifying the real-world location of a person, object, or photo using visual, environmental, or metadata clues.

### 🛠️ Tools:
- [SunCalc](https://suncalc.org)
- Google Earth & Street View
- OpenStreetMap
- InVID, Mapillary

### 🧠 Example:
A selfie posted with mountain peaks and sunlight can be triangulated using shadows, terrain, and background signs to find the exact location.

---

## 4. GeoGuessr (Gamified OSINT)

### 🎮 Concept:
**GeoGuessr** is a location-guessing game that builds skills critical for visual OSINT, such as:
- Reading terrain, signs, road markings
- Identifying language & region clues
- Estimating time and direction using the sun

### 🌍 Skills:
- Situational awareness
- Quick deduction
- Location validation

---

## 5. Creepiest OSINT Examples

### 😱 Concept:
OSINT can uncover shocking levels of detail — often from publicly shared information.

#### Real Examples:
- A pop star tracked through **eye reflection in a photo**
- War criminals geolocated using **dust, cloud shadows, and bomb craters**
- YouTubers doxxed using **1-second drone shots**

### 🚨 Lesson:
Even minor clues (signs, metadata, sounds) can lead to real-world consequences.

---

## 6. Discovering Email Addresses

### 📧 Concept:
Finding email addresses tied to individuals or organizations for reconnaissance or contact.

### 🔧 Tools:
- [Hunter.io](https://hunter.io)
- [EmailRep](https://emailrep.io)
- [Holehe](https://github.com/megadose/holehe)
- Google Dorks:  
  `site:example.com intext:@example.com`

### 🧠 Use Case:
Find a company’s email format → Guess target's email → Verify using Hunter or EmailRep.

---

## 7. Password OSINT

### 🔐 Concept:
Passwords often leak through public breaches, GitHub code, or personal patterns.

### 🛠️ Tools:
- [HaveIBeenPwned](https://haveibeenpwned.com)
- [Dehashed](https://dehashed.com)
- `cupp`, `Mentalist`, `Cewl` (wordlist builders)
- GitHub dorks, TruffleHog

### 🧠 Use Case:
From leaked password in a breach: `john1234` → Try `John12345!`, `John@2024`, etc.

---

## 8. Hunting Usernames & Passwords

### 🕵️ Concept:
Track **usernames** across platforms and discover **associated password leaks**.

### 🔧 Tools:
- [Sherlock](https://github.com/sherlock-project/sherlock)
- [Maigret](https://github.com/soxoj/maigret)
- [WhatsMyName](https://whatsmyname.app)
- [Scylla.sh](https://scylla.sh)

### Example:
`coolguy99` is found on Reddit → Profile pic leads to LinkedIn → Confirm real name → Found in breach with reused passwords.

---

## 9. Searching for People

### 🔎 Concept:
Combine public data (name, username, email, phone) to uncover real identities and patterns.

### 🛠️ Tools:
- [Pipl](https://pipl.com) *(paid)*
- [TrueCaller](https://truecaller.com)
- [SpiderFoot](https://www.spiderfoot.net)
- `PhoneInfoga`, `theHarvester`

### Steps:
1. Start with email/username  
2. Link to social media  
3. Check leaks and phone  
4. Use images to find location/faces

---

## 10. Vector Records in OSINT

### 🧠 Concept:
In OSINT/AI:
- A **vector** is a mathematical representation of data like faces, names, or texts.
- A **vector record** is stored in a **vector database** for similarity search.

In GIS:
- Vectors = lines, points, polygons representing geography

### 🛠️ Tools:
- Pinecone
- FAISS (Facebook AI Similarity Search)
- Weaviate
- OpenStreetMap (GIS)

### Example:
A face image is converted into a 128-dim vector → Searched in Pinecone → Returns similar faces.

---

## 11. Hunting Phone Numbers

### 📱 Concept:
Track and verify phone numbers tied to people, services, or leaks.

### 🛠️ Tools:
- [TrueCaller](https://truecaller.com)
- [Sync.me](https://sync.me)
- [PhoneInfoga](https://github.com/sundowndev/PhoneInfoga)
- WhatsApp, Telegram (profile discovery)
- Facebook Graph search

### Use Case:
Search `+923001234567` on TrueCaller → Name → Check WhatsApp profile → Reverse search image

---

## 12. Ethical Warning

**OSINT must be used ethically, legally, and with permission.**

### ✅ Allowed:
- Red teaming with permission
- Journalism, investigations
- Bug bounty recon
- Personal safety research

### ❌ Not allowed:
- Stalking
- Harassment or doxxing
- Unauthorized account access
- Illegal surveillance

---

## 📁 Want More?

Would you like:
- A downloadable **PDF cheatsheet**
- A **demo lab** with a fake target
- A Python **script collection** for OSINT?

Feel free to request more sections or GitHub-ready code.
