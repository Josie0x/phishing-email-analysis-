
## 🎣 Phishing Email Analysis — Suzain Billing Department
Home lab project analyzing a suspicious phishing email from my own inbox, documenting headers, attachments, IOCs, and IP/domain reputation

---

### Summary  
Analyzed a suspicious phishing email from `hardekonsen74@gmail.com` titled *“Suzain from Billing Department – Course Approved”*.  
Although SPF, DKIM, and DMARC all **passed**, the message contained an **empty body** and relied on the attached file `RSVOsEagEGY.pdf` to deliver a potential payload.

<img width="880" height="367" alt="Screenshot 2025-10-29 at 12 12 51 PM" src="https://github.com/user-attachments/assets/64bcb194-8817-41ef-8a36-b39e4f7782a6" />

---
### Findings  
- **Sender IP:** `209.85.220.41` (Google ASN15169)  
- **VirusTotal:** 1/95 flagged (Webroot: *Malicious / Criminal / Suspicious*)  
- **IOCs:**  
  - Email: `hardekonsen74@gmail.com`  
  - IP: `209.85.220.41`  
  - Attachment: `RSVOsEagEGY.pdf`
<img width="352" height="136" alt="Screenshot 2025-10-29 at 11 32 53 AM" src="https://github.com/user-attachments/assets/008eae73-75c0-4908-b7a8-c629f595eba6" />

---
<img width="1263" height="701" alt="Screenshot 2025-10-29 at 11 39 38 AM" src="https://github.com/user-attachments/assets/c86895e0-ec85-4cd6-97b8-da614af0a89d" />

---

#### Passive Analysis Steps Taken 📊
1. Saved raw `.eml` to project folder
2. Opened and inspected headers
3. Examined body text and HTML
4. Extracted sender IP, checked reputation on VirusTotal

---
#### MITRE ATT&CK Mapping  
- **T1566.001** – Phishing: Spearphishing Attachment  
- **T1204.002** – User Execution: Malicious File  

#### Kill Chain Stage 
Delivery → Exploitation

#### Recommended Remediation  
- Quarantine the email and block sender/IP.  
- Do not open attachments from unknown senders.  
- Reinforce phishing awareness for end users.
---

#### Next up 
 Malware Analyzation with FlareVM 🦠
 Boss of the SOC (BOTS) competition by Splunk 🏆
