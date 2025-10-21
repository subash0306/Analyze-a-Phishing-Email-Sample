# 🧾 Phishing Email Analysis Report

## Task 2 – Cyber Security Internship
**Topic:** Phishing Email Examination and Threat Analysis  
**Analyst:** [Your Name]  
**Date:** [Today’s Date]

---

## 1️⃣ Objective
The goal of this task is to analyze a suspicious email and identify phishing indicators by examining the sender, email headers, message body, and embedded links. This helps build awareness of phishing tactics and email-based social engineering threats.

---

## 2️⃣ Email Sample Overview

| Field | Detail |
|-------|---------|
| **Subject** | Microsoft account unusual signin activity |
| **Date** | 08 Sep 2023, 05:47:04 UTC |
| **From** | no-reply@access-accsecurity.com (spoofed) |
| **Return-Path** | bounce@thcultarfdes.co.uk |
| **Reply-To** | sotrecognizd@gmail.com |
| **Sender IP** | 89.144.44.2 |
| **Content Type** | text/html; charset="UTF-8" |
| **Attachments** | None |

---

## 3️⃣ SpamAssassin and Header Findings

| Category | Finding | Interpretation |
|-----------|----------|----------------|
| **SPF** | None | Domain not authorized to send mail from this IP |
| **DKIM** | None | Message not cryptographically signed |
| **DMARC** | Permerror | No policy / invalid configuration |
| **SPF Sender Domain** | thcultarfdes.co.uk | Not related to Microsoft |
| **Return Path** | bounce@thcultarfdes.co.uk | Different from From/Reply-To |
| **Reply-To** | sotrecognizd@gmail.com | Public freemail, unrelated to sender |
| **Spam Score (SCL)** | 5 | High spam probability |
| **Sender IP** | 89.144.44.2 | Suspicious external host |
| **AuthResult** | spf=none, dkim=none, dmarc=permerror | All authentication checks failed |

---

## 4️⃣ Email Body Examination

### Key Message:
> **“Unusual sign.in activity”**  
> We detected something unusual about a recent sign-in to your Microsoft account.  
> A user from **Russia/Moscow** just logged into your account.  
> If this wasn’t you, please report the user.  
> [**Report The User**] → (mailto link to `sotrecognizd@gmail.com`)

### Suspicious Elements:
- Urgent alert language creating fear of account compromise.
- “Report The User” button links to `mailto:sotrecognizd@gmail.com` (not Microsoft).
- Hidden tracking pixel from `http://thebandalisty.com/track/...`.
- Fake Microsoft formatting, incorrect “sign.in” usage, and unprofessional markup.
- Random code inside `<style>` tags—likely obfuscation.

---

## 5️⃣ Phishing Indicators

| # | Indicator | Description | Evidence |
|---|------------|--------------|-----------|
| 1 | Spoofed sender | From/Reply-To/Return-Path all differ | access-accsecurity.com / thcultarfdes.co.uk / gmail.com |
| 2 | Authentication failure | SPF/DKIM/DMARC missing | spf=none, dkim=none, dmarc=permerror |
| 3 | Suspicious IP | Not owned by Microsoft | 89.144.44.2 |
| 4 | Freemail Reply-To | Gmail used for reply | sotrecognizd@gmail.com |
| 5 | Tracking pixel | Hidden image beacon | thebandalisty.com/track/... |
| 6 | Urgent message | Fear-based alert | Body text |
| 7 | Grammar errors | “sign.in”, malformed text | Body text |
| 8 | Non-Microsoft URLs | No official domain links | mailto Gmail link |
| 9 | HTML-only email | No plain text version | SpamAssassin body tag |

---

## 6️⃣ Analysis Summary
✅ **Indicators of Phishing:**  
- Spoofed sender identity and domain mismatch.  
- Authentication failures (SPF/DKIM/DMARC).  
- Freemail reply-to and hidden tracking pixel.  
- Urgency-based message design.  
- Grammar and structure errors.  

🚫 **Conclusion:**  
This is a **phishing email** impersonating Microsoft to trick users into replying or sharing credentials. It uses social engineering and spoofed headers.

---

## 7️⃣ Recommended Mitigation Steps
1. Do **not click** or reply to links in the email.
2. **Report** as phishing to Microsoft or your email provider.
3. **Block** sender domains (`access-accsecurity.com`, `thcultarfdes.co.uk`, `thebandalisty.com`).
4. Enable **Multi-Factor Authentication (MFA)** on accounts.
5. Run **antivirus scans** if any link was clicked.
6. **Educate users** on verifying links before action.

---

## 8️⃣ Tools Used
| Tool | Purpose |
|------|----------|
| SpamAssassin | Automated spam scoring |
| Online Header Analyzer | Review SPF/DKIM/DMARC results |
| DNS Lookup Tools | Domain reputation check |
| Manual HTML Inspection | Identify links and trackers |
| Email Client (Outlook) | Header extraction and viewing |

---

## 9️⃣ Outcome
**Learning Outcome:**  
Developed hands-on understanding of phishing detection, spoofed domain analysis, and email authentication.  

**Key Skills:**  
- Header forensics  
- Spoof detection  
- Threat pattern analysis  
- Social engineering awareness

---

## 🔗 Submission
**GitHub Repository:** `https://github.com/yourusername/phishing-email-analysis`  
**Submission Link:** [https://forms.gle/8Gm83s53KbyXs3Ne9](https://forms.gle/8Gm83s53KbyXs3Ne9)

---
