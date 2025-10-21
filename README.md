# README – Phishing Email Analysis

##  Project Overview
This repository contains a **phishing email analysis report** created for the **Cyber Security Internship (Task 2)**. The objective is to analyze a suspicious email sample and identify indicators of phishing, spoofing, and social engineering.

---

##  Objective
To identify and explain phishing characteristics in an email pretending to be a Microsoft security alert. The analysis includes:
- Header analysis (SPF, DKIM, DMARC)
- Link inspection
- Sender authenticity verification
- Grammar and urgency checks

---

##  Tools Used
| Tool | Purpose |
|------|----------|
| **SpamAssassin** | Automated spam and header scoring |
| **Online Header Analyzer** | Check SPF, DKIM, DMARC results |
| **Email Client (Outlook)** | View message headers |
| **Manual HTML Inspection** | Identify suspicious links and trackers |
| **DNS/WHOIS Lookup** | Domain and IP reputation checking |

---

##  Files Included
| File | Description |
|------|-------------|
| `phishing_report.md` | Full report explaining phishing indicators and conclusions |
| `README.md` | Overview of task, objectives, and tools used |
| *(Optional)* screenshots/ | Supporting visuals like header analysis or email body |

---

##  Summary of Findings
- Sender spoofed using mismatched domains (`access-accsecurity.com`, `thcultarfdes.co.uk`, and Gmail).
- SPF, DKIM, and DMARC authentication all **failed**.
- Hidden tracking pixel linked to `thebandalisty.com`.
- Urgent, fear-based messaging encouraging immediate action.
- Grammar and structural errors (e.g., “sign.in”).

**Conclusion:** The email is a **confirmed phishing attempt** impersonating Microsoft.

---
