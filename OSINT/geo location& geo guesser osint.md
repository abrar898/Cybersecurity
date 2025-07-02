# 🧭 Geolocation in OSINT

## 📌 What is Geolocation in OSINT?
Geolocation is the process of identifying the **physical location** (city, building, coordinates) of a person, object, or event using available **open-source data** such as:
- Images  
- Videos  
- Metadata  
- Social media posts  
- News articles  
- Maps  

---

## 🧰 Methods for Identifying Geographical Locations

### 1. 🔍 Visual Clues from Images & Videos
**Analyze:**
- Language on signs (e.g., Urdu → Pakistan)  
- Street signs or store names  
- Vehicles (license plates, models)  
- Building architecture  
- Terrain, climate, or vegetation  
- Traffic direction (left-hand vs right-hand)  

**Example:** If you see "KFC" and the signboard is in Arabic, it might be a Gulf country.

---

### 2. 📸 EXIF Data (Metadata in Images)
**Possible Data:**
- GPS coordinates  
- Camera/device info  
- Timestamp  

**Tools:**
- `exiftool`  
- [exif.regex.info](https://exif.regex.info)  
- [fotoforensics.com](https://fotoforensics.com)  

---

### 3. 🔁 Reverse Image Search
**Purpose:**
- Trace origin  
- Find similar angles or scenes  

**Tools:**
- Google Images  
- Yandex  
- TinEye  

---

### 4. 🗺️ Map Matching
Use satellite and street maps to compare image details.

**Tools:**
- Google Maps  
- Google Earth  
- OpenStreetMap  
- Wikimapia  
- Mapillary  
- Zoom Earth  

---

### 5. ☀️ Sun and Shadow Analysis
**Purpose:** Estimate time and hemisphere based on shadows.

**Tool:** [SunCalc.net](https://suncalc.net)

---

### 6. 📱 Social Media Geolocation
Clues from:
- Geotagged posts  
- Hashtags (e.g., #LahoreRain)  
- Landmarks in background  

**Platforms:**
- Instagram  
- Twitter / X  
- Facebook  
- YouTube  

---

### 7. 🛰️ IP Address Lookup
**Purpose:** Approximate a location from an IP address.

**Tools:**
- [ipinfo.io](https://ipinfo.io)  
- [iplocation.net](https://iplocation.net)  
- MaxMind  

⚠️ Note: IP data can be inaccurate (VPNs, proxies, NAT).

---

## 🎓 Example Case Study: Image Geolocation
- Start with a protest image  
- No match in reverse search  
- See hotel sign: “Hotel Gulberg”  
- Google it: “Hotel Gulberg Pakistan”  
- Match image via Street View  
- Analyze shadows for time of day  

---

## ✅ Summary Table

| Method                   | Description                            | Tools                                |
|--------------------------|----------------------------------------|--------------------------------------|
| Visual Clue Analysis     | Landmarks, language, terrain           | Brain + Street View                  |
| EXIF Metadata            | GPS and device info                    | exiftool, regex.info                 |
| Reverse Image Search     | Match images                           | Google, Yandex, TinEye               |
| Satellite/Street Mapping | Compare map features                   | Google Maps, Earth, Wikimapia        |
| Sun/Shadow Analysis      | Estimate time/hemisphere               | SunCalc                              |
| Social Media Investigation| Posts, hashtags, backgrounds          | Facebook, X, Instagram               |
| IP Geolocation           | Approximate physical IP location       | ipinfo.io, iplocation.net            |

---

# 🌍 What is GeoGuessr?

**GeoGuessr** is an online game where players guess the real-world location shown in a 360° street image.

---

## 🎮 How It Works
- You’re dropped somewhere in Street View  
- Use visual clues to guess location  
- Guess on a map  
- Get up to 5000 points per round  

---

## 🔍 What Clues Can You Use?

| Clue Type    | What to Look For                        |
|--------------|------------------------------------------|
| Language     | Signboards, ads                          |
| Road Signs   | Shape, text, style                       |
| Vehicles     | License plate, left/right driving        |
| Nature       | Vegetation, climate                      |
| Architecture | Design and materials of buildings        |
| People       | Clothing, cultural hints                 |
| Shadows      | Hemisphere and time estimation           |

---

## 🌐 Game Modes
- **World** – Random location  
- **Famous Places** – Landmarks only  
- **Country Specific** – E.g., India, Pakistan  
- **Battle Royale** – Compete with others  
- **Streaks** – Guess countries repeatedly  

---

## 🧠 Benefits of Playing GeoGuessr
- Develops visual reasoning  
- Enhances OSINT geolocation skills  
- Expands geography knowledge  
- Fun + educational  

---

## 🔧 Tools for GeoGuessr OSINT Practice

| Tool                     | Use Case                          |
|--------------------------|-----------------------------------|
| Google Translate         | Translate signboards              |
| SunCalc.net              | Analyze sun angle                 |
| Mapillary/OpenStreetCam  | Alternate street view             |
| GeoTips.net              | Country-specific visual tips      |
| License Plate Guides     | Regional vehicle identifiers      |

---

## 🔗 Where to Play
**Official site:** [https://www.geoguessr.com](https://www.geoguessr.com)  
⚠️ Free account has limited daily plays.

