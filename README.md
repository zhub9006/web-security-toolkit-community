# Web Security Community Toolkit

A community-driven resource for web security practitioners, combining **privacy compliance insights from clinical research** with **practical guidance** for building secure, privacy-first web applications — plus a guide to Portland-area venues for security workshops and meetups.

---

## 🛡️ Key Privacy Takeaways from Clinical Trials

Our review of recent ClinicalTrials.gov studies (2023–2026) reveals privacy and data-protection practices that translate directly to web security:

### 1. Data De-identification at Source
**NLM Scrubber (NCT02795806)** — The U.S. National Library of Medicine developed an automated tool that recognizes and removes all 18 categories of Personally Identifiable Information (PII) defined by HIPAA from clinical text. Key principle: **strip identifiers before any secondary use or sharing**, using both automated and manual verification.

> 🔗 *Web security parallel:* Implement field-level data masking and anonymization in your application before logs, analytics, or third-party data sharing.

### 2. Locally-Deployed Processing (Data Never Leaves Your Infrastructure)
**Privacy-Preserving OCR-LLM System (NCT07449429)** — This study deploys OCR and LLM inference locally (on-premise), so patient HPI images are never sent to external APIs. De-identified text is extracted and processed in-house; no individual participant data is shared publicly.

> 🔗 *Web security parallel:* For sensitive user data, keep processing on your own servers or use on-device computation. Avoid sending raw PII to third-party APIs (including AI/ML services) unless absolutely necessary and properly de-identified.

### 3. Layered Data Protection (Technical + Administrative + Physical)
**Rehabilitation Chatbot Trial (NCT07308691)** — The study applied password-protected systems, anonymization of stored data, locked physical storage for records, and secure destruction after the retention period. All processes passed Institutional Review Board (IRB) ethics approval with informed consent.

> 🔗 *Web security parallel:* Apply defense-in-depth — encrypt data at rest and in transit, enforce access controls (RBAC), audit access logs, and define data retention/deletion policies that are technically enforced.

### 4. Pseudonymisation with Controlled Access
**EGFR Pathogenic Variants Study (NCT06562491)** — Patient data was pseudonymised at each site into secure, centre-specific Excel files. Access was restricted to the Principal Investigator + max 2 collaborators. Data was transmitted via France's secure national RENATER platform and governed by CNIL regulations; patients could opt out.

> 🔗 *Web security parallel:* Use pseudonymous identifiers in your databases, enforce least-privilege access, transmit data over secure channels, and give users meaningful opt-out/consent controls (GDPR/CCPA compliance).

### Summary Table

| Practice | Clinical Study | Web Security Adaptation |
|---|---|---|
| Automated PII detection & removal | NLM Scrubber (NIH) | Data masking / field-level redaction |
| On-premise data processing | OCR-LLM Privacy Study (China/US) | Self-hosted services; no raw PII to third parties |
| Password + encryption + physical security | Rehab Chatbot (Hong Kong) | Defense-in-depth: encrypt, access-control, audit |
| Pseudonymisation + least-privilege access | EGFR Study (France, CNIL) | Pseudonymous IDs, RBAC, secure transfer |
| Informed consent + opt-out | All studies | Consent management UI; data subject rights |
| IRB / ethics review | All studies | Privacy impact assessments (PIAs) |

---

## 🏛️ Portland Area Venues for Security Meetups & Workshops

All locations are within **~2 km of downtown Portland, Oregon**.

### Community & Workshop Spaces

| Venue | Address | Best For | Notes |
|---|---|---|---|
| **Portland Community College — Downtown Center** | 722 SW 2nd Ave | Workshops, classrooms | Purpose-built for training; AV equipment available |
| **Oregon Convention Center** | 777 NE MLK Jr Blvd | Large events, conferences | Multiple breakout rooms; downtown location |
| **Portland Art Museum** | 1219 SW Park Ave | Cultural meetups, presentations | Iconic venue; event rental available |
| **Oregon Historical Society** | 1200 SW Park Ave | Community events, talks | Adjacent to the museum district |
| **Portland State University** | 1825 SW Broadway | Academic-style talks, panels | Campus venues available for community events |

### Cafes & Informal Meetup Spots

| Venue | Address | Highlights |
|---|---|---|
| **Portal Tea** | 734 NW 23rd Ave | Indoor seating, free WiFi, tea-focused |
| **Case Study Coffee Roasters** | 1400 NW 23rd Ave | WiFi, outdoor seating, great for small groups |
| **Starbucks (23rd & Burnside)** | 2328 W Burnside | WiFi, wheelchair accessible, reliable meetup spot |

### Restaurants for Group Gatherings

| Venue | Address | Cuisine | Wheelchair Accessible |
|---|---|---|---|
| **Papa Haydn** | 635 NW 23rd Ave | Regional American | ✅ |
| **Pepino's** | 914 NW 23rd Ave | Mexican | — |
| **Jo Bar** | 715 NW 23rd Ave | Pub / Gastropub | ✅ |
| **Hop City Tavern** | 921 SW 6th Ave (Hilton) | American | ✅ |

---

## 🚀 Getting Started

1. **Fork this repo** to add your own security resources
2. **Run a privacy audit** using the practices above — start with a PIA
3. **Host a workshop** at one of the Portland venues listed
4. **Share findings** with the community via issues and PRs

### Recommended Workshop Topics
- Implementing field-level data masking in web apps
- On-premise vs. third-party AI/ML: when to keep data local
- Building consent management flows that actually work
- Defense-in-depth for user data at rest and in transit
- Privacy-by-design in modern web frameworks

---

## 📄 License

MIT — feel free to use, adapt, and share.

---

## 🙏 Acknowledgements

Clinical trial data sourced from [ClinicalTrials.gov](https://clinicaltrials.gov). Venue data sourced from [OpenStreetMap](https://openstreetmap.org).