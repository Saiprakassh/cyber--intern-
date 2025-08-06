# 🎯 Phishing Email Analysis – Cyber Security Internship Task 2

## ✅ Objective
To identify and document phishing indicators in a suspicious email sample using manual analysis and online tools. The aim is to improve awareness of email-based threats and phishing detection techniques.

---

## 📧 Sample Phishing Email

- **From:** Google Alerts `<security@google-alerts.com>`
- **To:** user@example.com  
- **Subject:** Immediate Action Required: Suspicious Sign-in Detected  
- **Message ID:** suspicious-id@google-alerts.com  
- **Date:** Thu, 07 Aug 2025 11:12:03 +0000

---

## 🔍 Message Header Analysis Using Google Admin Toolbox

### 📌 Authentication Checks:

| Check  | Status | Details |
|--------|--------|---------|
| **SPF** | ❌ FAIL | IP `203.0.113.55` is not authorized to send emails on behalf of `google-alerts.com`. |
| **DKIM** | ❌ None | No DKIM signature found for `google-alerts.com`. |
| **DMARC** | ❌ FAIL | DMARC policy failed; domain `google-alerts.com` does not pass alignment. |

### 🛠 Technical Breakdown:

- **Sending IP Address:** `203.0.113.55` (flagged as suspicious)
- **Received From:** `smtp.scamserver.org`
- **Mail Server:** `mail.clientserver.com`
- **HELO:** `smtp.scamserver.org`
- **Return Path:** `<security@google-alerts.com>`

---

## ⚠️ Indicators of Phishing:

- ❗ **Sender spoofing:** Appears to be from `Google Alerts`, but the sending IP is unauthorized and hosted on a suspicious server.
- ❗ **Failed SPF, DKIM, and DMARC:** Indicates the email fails standard email authentication protocols.
- ❗ **Urgency in Subject Line:** “Immediate Action Required” is a typical tactic used in phishing attacks.
- ❗ **Unknown Mail Route:** Message passed through unrecognized or suspicious servers (`smtp.scamserver.org`).

---

## ✅ Conclusion:

This email is a **phishing attempt**. It impersonates a trusted brand (Google) and urges the user to act immediately while failing all major email authentication checks (SPF, DKIM, DMARC).  
Such emails should be reported and never interacted with.

---

## 🧰 Tools Used:

- [Google Admin Toolbox - Message Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/)
- Manual inspection of email metadata

---

## 📸 Screenshots

1. **Message Header Analysis Summary:**  
   ![Message Header Summary](./Message%20header%20analysis.png)

2. **Raw Header Content:**  
   ![Raw Header](./Messageheader.png)
