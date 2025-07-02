# 📧 Discovering Email Addresses Using OSINT (Ethical Techniques)

Finding someone’s email address using OSINT is a powerful part of reconnaissance in bug bounty, pentesting, social engineering, or threat intel gathering.

---

## 🔍 Why Discover Email Addresses?
- For phishing simulations (red teaming)
- For password dump lookups
- For social media footprinting
- For username enumeration
- For contacting a target individual or organization

---

## 🧰 Common OSINT Techniques to Discover Email Addresses

### 1. 🔎 Google Dorking
Example:
site:example.com intext:"@example.com"

yaml
Copy
Edit

Other useful dorks:
"email * * example.com"
"contact * * example.com"

yaml
Copy
Edit

---

### 2. 🛠️ Email Discovery Tools & Platforms
| Tool | Description |
|------|-------------|
| Hunter.io | Find email patterns and known emails |
| Emailformat.com | Common company email formats |
| VoilaNorbert / Snov.io | Guess + verify emails |
| RocketReach / Lusha | Lookup for professionals |
| Clearbit | People enrichment API |

---

### 3. 💾 Check Data Breach Dumps
- **HaveIBeenPwned.com**
- **Dehashed (paid)**
- **CLI tools**: `holehe`, `ghunt`, `Maigret`

Example:
holehe target@example.com

yaml
Copy
Edit

---

### 4. 🔍 Social Media OSINT
- **LinkedIn**: Emails often public
- **Twitter**: Phrases like “email me at”
- **GitHub**: Check commits with:
git log | grep @

yaml
Copy
Edit
- **Facebook/Instagram**: About/contact sections

---

### 5. 💡 Email Pattern Guessing
| Name | Possible Emails |
|------|------------------|
| John Doe | john@example.com, john.doe@example.com, jdoe@example.com |

Use tools like Hunter.io for verification.

---

### 6. 🌐 Company “Contact Us” Pages
- Look for emails like:
  - info@company.com
  - support@company.com
  - ceo@company.com

---

### 7. 🗂️ WHOIS Lookup
Unredacted domains may reveal:
- Registrant’s email
- Admin contact email

Command:
whois example.com

yaml
Copy
Edit

---

### 8. 🖼️ EXIF & File Metadata
Emails might be embedded in:
- PDFs
- Word docs
- Images

Tools:
- `exiftool`
- `pdfinfo`
- `strings`

---

## 🚨 Ethics & Legal Warning
Only use these techniques ethically and legally:
- CTFs
- Bug bounty
- Research with permission

Do **not** use for fraud, harassment, or unauthorized access.

---

## ✅ Summary Table

| Technique | Tool/Example | Use Case |
|----------|--------------|----------|
| Google Dorks | `site:domain.com "@domain.com"` | Find indexed emails |
| Email Tools | Hunter.io, Snov.io | Guess/verify |
| Breach Dumps | HaveIBeenPwned, holehe | Leaked emails |
| Social Scraping | GitHub, LinkedIn | Dev/employee emails |
| WHOIS | `whois example.com` | Domain contact info |
| Metadata | `exiftool`, `pdfinfo` | Embedded email detection |

---

Would you like a tool/script to automate this discovery process?
