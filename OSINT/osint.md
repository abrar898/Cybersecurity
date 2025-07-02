# 🕵️ OSINT Toolkit & Field Guide

This README provides a detailed overview of essential OSINT concepts, tools, techniques, and examples related to discovering and analyzing **usernames, passwords, emails, phone numbers, physical locations**, and more — all using open-source, legal, and ethical methods.

---

## 📖 Table of Contents

- [1. Footprinting vs Fingerprinting](#1-footprinting-vs-fingerprinting)
- [2. Image Reversing & EXIF Data](#2-image-reversing--exif-data)
- [3. Geolocation OSINT](#3-geolocation-osint)
- [4. GeoGuessr (Gamified OSINT)](#4-geoguessr-gamified-osint)
- [5. Creepiest OSINT Examples](#5-creepiest-osint-examples)
- [6. Discovering Email Addresses](#6-discovering-email-addresses)
- [7. Password OSINT](#7-password-osint)
- [8. Hunting Usernames & Passwords](#8-hunting-usernames--passwords)
- [9. Searching for People](#9-searching-for-people)
- [10. Vector Records](#10-vector-records)
- [11. Hunting Phone Numbers](#11-hunting-phone-numbers)

---

## 1. Footprinting vs Fingerprinting

**Footprinting**: Passive information gathering about a target (e.g., domains, emails, technologies used).  
**Fingerprinting**: Active identification of a system or service (e.g., OS, web server version).

| Footprinting | Fingerprinting |
|--------------|----------------|
| Passive      | Active         |
| Uses WHOIS, DNS | Uses nmap, banner grabbing |
| Safer/legal  | Can trigger alarms |

---

# 🖼️ Image Reversing and EXIF Data Analysis in OSINT

This README covers two powerful image-based OSINT techniques: **Reverse Image Search** and **EXIF Data Analysis**. These methods help investigators verify image authenticity, source, and metadata.

---

## 1. 🖼️ Image Reversing (Reverse Image Search)

### 🔍 Definition:
Image reversing is the process of using a reverse image search engine to find the **source**, **history**, or **copies** of an image across the internet.

### 🎯 Purpose in OSINT:
- Identify the original source of an image  
- Track where else the image appears online (forums, social media, news, etc.)  
- Find similar or edited versions of the image  
- Discover the context or detect misinformation/fake news  

### 🔧 Tools Used:
- [Google Reverse Image Search](https://images.google.com)  
- [TinEye](https://tineye.com)  
- Yandex Image Search – Often better at finding people & objects  
- Bing Visual Search  

### 📌 Use Case Example:
You find a photo on Twitter claiming a protest occurred yesterday. Using reverse image search, you discover the **same image was published 3 years ago** in a news article. ✅ This helps debunk misinformation.

---

## 2. 🧾 EXIF Data (Exchangeable Image File Format)

### 🔍 Definition:
EXIF data is **metadata automatically embedded** in an image file (usually by a digital camera or smartphone) that stores details about how, when, and where the image was taken.

### 🧠 Common EXIF Fields:
- Date and time the photo was taken  
- Device model and manufacturer (e.g., iPhone 13 Pro)  
- Camera settings (aperture, shutter speed, ISO)  
- GPS coordinates (latitude, longitude)  
- Software used to edit or process the image  

### 🎯 Purpose in OSINT:
- Track the location where a photo was taken (if GPS is enabled)  
- Learn about the device and software used  
- Identify manipulation (e.g., EXIF shows editing in Photoshop)  
- Cross-reference time/date for timeline building  

### 🔧 Tools to View EXIF Data:
**Online EXIF Viewers:**
- [Exif Regex Info](https://exif.regex.info)
- [FotoForensics](https://fotoforensics.com)

**Command-line Tools:**
- `exiftool` (Linux/Mac/Windows)

**Mobile Apps:**
- EXIF Viewer (Android/iOS)

### ⚠️ Important Notes:
- Many **social media platforms strip EXIF data** when images are uploaded  
- Some tools can **spoof or delete EXIF data** to avoid tracking  

### 📌 Use Case Example:
An image is leaked online. You extract the EXIF data and find GPS coordinates—plug them into Google Maps and pinpoint the **exact building** where the photo was taken.

---

## 🧠 Summary Table

| Feature              | Image Reversing                   | EXIF Data Analysis                |
|---------------------|-----------------------------------|-----------------------------------|
| **Focus**           | Find image source & context       | Extract metadata from image       |
| **Tools**           | Google, Yandex, TinEye            | exiftool, FotoForensics, Regex    |
| **Used For**        | Source tracing, fake news check   | Geolocation, device, timeline     |
| **Data Type**       | Visual image matching             | Embedded metadata                 |
| **OSINT Role**      | Verifying authenticity            | Finding location/timeline/device  |

---

📂 This file is part of an OSINT learning series. Contributions and examples are welcome.


---

## 3. Geolocation OSINT

Using visual, metadata, and contextual clues from media to identify real-world locations.

**Usage:** Locating where a photo/video was taken using landmarks, weather, shadows.

**Tools:**
- [SunCalc](https://suncalc.org)
- Google Earth
- OpenStreetMap
- InVID plugin

---

## 4. GeoGuessr (Gamified OSINT)

**GeoGuessr** is a game that drops you in a random location (Street View), and you guess where you are using visual clues.

**Why it matters in OSINT:** Trains your **visual deduction, mapping, and clue analysis** skills.

**Skills Tested:**
- Reading signs, languages, shadows
- Identifying vegetation and terrain
- Estimating based on architecture

---

## 5. Creepiest OSINT Examples

Real-world shocking use cases of OSINT:
- Finding a person via reflections in their **eyes**
- Rebuilding identities from **YouTube videos**
- Using **satellite imagery** to track people
- **EXIF data** revealing photo locations

**Lesson:** Even innocent content can leak serious data.

---

## 6. Discovering Email Addresses

### 🎯 Goal
Find and verify target emails.

**Tools:**
- [Hunter.io](https://hunter.io)
- [EmailRep](https://emailrep.io)
- [Holehe](https://github.com/megadose/holehe)
- Google Dorks:  
  `site:example.com intext:@example.com`

**Example Use Case:**  
Find CEO's email from company blog using `hunter.io` and verify with `emailrep.io`.

---

## 7. Password OSINT

### 🎯 Goal
Discover leaked or weak passwords.

**Sources:**
- Data breaches
- Paste sites
- GitHub commits
- Public documents

**Tools:**
- [HaveIBeenPwned](https://haveibeenpwned.com)
- [Dehashed](https://dehashed.com)
- `cupp`, `cewl`, `Mentalist` (wordlist builders)
- `TruffleHog`, `GitLeaks`

---

## 8. Hunting Usernames & Passwords

### 🎯 Goal
Track username reuse across platforms and collect passwords from leaks.

**Tools:**
- [WhatsMyName](https://whatsmyname.app)
- [Sherlock](https://github.com/sherlock-project/sherlock)
- [Maigret](https://github.com/soxoj/maigret)
- [Scylla.sh](https://scylla.sh)

**Example:** Use `Sherlock` to find a user’s social profiles from one username.

---

## 9. Searching for People

### 🎯 Goal
Find personal information (location, job, photos, connections).

**Tools:**
- [Pipl.com](https://pipl.com)
- [Yandex Reverse Image](https://yandex.com/images)
- [LinkedIn](https://linkedin.com)
- `PhoneInfoga`, `Spiderfoot`

**Example Use Case:**
Start with email → discover name → reverse image search → link to Facebook/LinkedIn.

---

## 10. Vector Records

### Definition:
- In OSINT/AI: Vectors = math representations of data (e.g., face embeddings, text similarity)
- In GIS: Vectors = map features (roads, buildings)
- In Cyber: Attack vector records = document known intrusion methods

**Use Case:**
Store faces or usernames as vectors → use similarity search to detect linked identities.

**Tools:**
- Pinecone
- FAISS
- Milvus

---

## 11. Hunting Phone Numbers

### 🎯 Goal
Find details linked to a phone number (identity, location, social apps).

**Tools:**
- [TrueCaller](https://truecaller.com)
- [Sync.Me](https://sync.me)
- [PhoneInfoga](https://github.com/sundowndev/PhoneInfoga)
- WhatsApp / Telegram profile checking

**Example Use Case:**
Input number in TrueCaller → get name → add to WhatsApp → collect DP & last seen → reverse search profile image.

---

## ⚠️ Ethics Notice

This information is for **legal, ethical, and educational use only**. Never use OSINT to:
- Harass or stalk
- Hack accounts
- Access private systems

Always get permission when doing corporate or red team OSINT.

---

## 👨‍💻 Want a Hands-On Lab?

Let us know if you’d like:
- A downloadable **OSINT PDF cheat sheet**
- A practice lab (fake persona + challenge)
- A step-by-step **walkthrough**

---
