# Phishing Email Analysis — Suzain Billing Department

## Summary
Home lab project analyzing a suspicious phishing email from my own inbox, documenting headers, attachments, IOCs, and IP/domain reputation for cybersecurity learning and demonstration.

---

## Email Metadata (Headers)
- **From:** Ch Hi <hardekonsen74@gmail.com>
- **To:** Josiahcharles589@gmail.com
- **Subject:** Suzain from Billing Department course approved . 10 Oct 2025
- **Date:** Fri, 10 Oct 2025 16:13:05 +0000
- **Message-ID:** <CABB2B8ZoV_4TmS25jPA2QVj3+DLy1y0-r5HaS5M9Ly7jOkfLQQ@mail.gmail.com>
- **SPF:** PASS
- **DKIM:** PASS
- **DMARC:** PASS
- **Return-Path:** <hardekonsen74@gmail.com>
- **Received Path:** Gmail servers (see raw headers)

![Headers screenshot](reports/headers.png)

---

## Message Body
- **Plain text / HTML content:** `<div dir="ltr"></div>` (empty HTML body)
- **Displayed link text:** None / N/A
- **Actual URL:** None / N/A

---

## URLs/IP Reputation
- **Sender IP:** 209.85.220.41
- **Owner / ASN:** Google (AS15169)
- **Location:** US
- **Community Score:** -32
- **Security Vendors:** 1/95 flagged (Webroot: Malicious / Criminal / Suspicious)
- **Notes:** IP belongs to Gmail infrastructure; likely false positive.

![VirusTotal screenshot](reports/ip_virustotal.png)

---

## Attachments
| File Name | Type | Size | Hash (SHA256) | Notes |
|-----------|------|------|---------------|-------|
| RSVOsEagEGY.pdf | PDF | <FILL IN> | <FILL IN> | Suspicious attachment; not opened |

![Attachment screenshot](reports/attachment.png)

---

## Domain Info
- **Domain:** gmail.com  
- **Domain Age:** ~1997  
- **Registrar:** Google LLC  
- **SPF Pass/Fail:** PASS

---

## Passive Analysis Steps Taken
1. Saved raw `.eml` to project folder
2. Opened and inspected headers in Apple Mail / Thunderbird
3. Examined body text and HTML (no links)
4. Extracted sender IP, checked reputation on VirusTotal
5. Saved attachment (no execution), recorded file name and hash

---

## Indicators of Compromise (IOCs)
- **Email:** hardekonsen74@gmail.com
- **IP:** 209.85.220.41
- **Attachment:** RSVOsEagEGY.pdf (hash: <FILL IN>)
- **Links:** None

---

## Recommended Remediation
- Block IP / domain in email filters if malicious activity observed
- Quarantine the message
- Do **not** open attachment
- Educate users on phishing awareness

---

## Next Up
 Boss of the SOC (BOTS) competition by Splunk 🏆
