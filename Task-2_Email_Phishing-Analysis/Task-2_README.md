# 🛡️ Task 2 — Phishing Email Analysis (Let's Defend Hands-on)

**Project:** Cyber Security Internship — ElevateLabs Pvt. Ltd.
**Task:** 2 — Phishing Email Analysis
**Author:** Pratyush Raj
**Date:** 22-10-2025
**Platform Used:** LetsDefend — Phishing Email Analysis Course

---

## 🔍 Overview

This repository documents my **hands-on Phishing Email Analysis** performed on the LetsDefend platform as part of my Cyber Security Internship program with **ElevateLabs Pvt. Ltd.**
The objective was to analyze phishing emails, identify attack patterns, perform header/static/dynamic analysis, and apply real-world SOC investigation methods.

---

## 📚 Table of Contents

1. [About the Project](#about-the-project)
2. [Topics Covered](#topics-covered)
3. [Tools & Platforms Used](#tools--platforms-used)
4. [Lab Practice Sections](#lab-practice-sections)
5. [Repository Structure](#repository-structure)
6. [Screenshots](#screenshots)
7. [Certificate / Proof of Completion](#certificate--proof-of-completion)

---

## 📖 About the Project

Phishing Email Analysis is a critical part of SOC (Security Operations Center) operations. The goal is to detect and mitigate phishing threats by analyzing:

* Suspicious sender addresses
* Email headers & routing paths
* Malicious attachments or links
* Behavioral indicators via static and dynamic analysis

This project showcases the full process learned and practiced through the LetsDefend labs, aligned with professional SOC workflows.

---

## 🧠 Topics Covered

* Introduction to Phishing & Cyber Kill Chain Delivery Phase
* Information Gathering (SPF, DKIM, DMARC)
* Email Header Analysis
* Static & Dynamic Analysis
* Additional Techniques (Cloud-hosted Phishing, Form-based scams)
* SOC Alert Practice & Incident Response
* Final Challenge: Phishing Email Investigation

---

## 🧰 Tools & Platforms Used

| Tool                                 | Purpose                           |
| ------------------------------------ | --------------------------------- |
| **LetsDefend**                       | Main training & lab environment   |
| **MXToolbox**                        | Email header & MX record analysis |
| **VirusTotal**                       | URL and file reputation scanning  |
| **Cisco Talos Intelligence**         | IP reputation checking            |
| **AbuseIPDB**                        | Check past malicious IP reports   |
| **AnyRun / Hybrid Analysis / VMRay** | Sandbox dynamic analysis          |
| **Browserling**                      | Safe web browsing in isolation    |

---

## 🧪 Lab Practice Sections

Each topic from the LetsDefend Phishing Email Analysis course included hands-on exercises:

### 1. Introduction to Phishing

> Learned how phishing exploits human psychology to lure users into performing unsafe actions.

### 2. Information Gathering

> Practiced SPF/DKIM/DMARC verification and SMTP header tracing.

### 3. Email Header Analysis

> Investigated sender authenticity using MXToolbox & manual header inspection.

### 4. Static & Dynamic Analysis

> Performed safe examination of URLs and attachments using VirusTotal and sandbox tools.

### 5. Additional Techniques

> Identified modern phishing delivery mechanisms such as Google Drive or form-based scams.

### 6. SOC Alerts (Hands-on)

> Investigated the following incidents:
>
> * SOC141 — Phishing URL Detected
> * SOC140 — Phishing Mail Detected (Suspicious Task Scheduler)
> * SOC120 — Internal-to-Internal Phishing Mail
> * SOC114 — Malicious Attachment Detected (Phishing Alert)

### 7. Challenge: Phishing Email

> Conducted end-to-end investigation of a phishing email sample, analyzed headers, and validated domain/IP authenticity.

---

## 🗂️ Repository Structure

```
task-2-phishing-email-analysis/
├── README.md
├── report/
│   ├── phishing-email-analysis-report.md
│   ├── phishing-email-analysis-report.pdf
│   └── screenshots/
│       ├── screenshot-01-email-example.png
│       ├── screenshot-02-header-view.png
│       ├── screenshot-03-virus-total.png
│       ├── screenshot-04-sandbox-analysis.png
│       └── screenshot-05-soc-alert.png
├── artifacts/
│   ├── sample-email.txt
│   ├── headers.txt
│   └── letsdefend_certificate.png
└── .gitignore
```

---

## 🖼️ Screenshots

📸 Each section includes practical evidence from the LetsDefend labs. 

---

## 🏅 Certificate / Proof of Completion

Once the Let's Defend course is completed, include:

* Completion badge or certificate screenshot
* Let's Defend course progress summary

These will serve as verification of the hands-on experience gained.



---

## 💬 Commit Message Template

```bash
git add .
git commit -m "Task 2: Add LetsDefend phishing email analysis report and screenshots"
git push origin main
```

---

## ✅ Conclusion

This repository represents my applied understanding of phishing analysis through a structured SOC-oriented workflow using the LetsDefend environment.
It demonstrates practical competency in identifying, analyzing, and documenting phishing incidents with professional rigor.

---

**© 2025 Pratyush Raj — ElevateLabs Pvt. Ltd. Cyber Security Internship**
