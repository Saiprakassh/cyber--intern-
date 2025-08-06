📧 Phishing Email Header Analysis – Sample Report
🎯 Objective
To detect and analyze phishing characteristics using email header metadata. This sample is analyzed using the Google Admin Toolbox – Message Header Analyzer.

🧪 Sample Header Metadata (Summarized)
Return-Path: security@google-alerts.com

Received from: smtp.scamserver.org (203.0.113.55)

SPF: ❌ fail – IP not permitted by sender domain

DKIM: ❌ none – No DKIM signature present

DMARC: ❌ fail – Domain policy failed

From: Google Alerts <security@google-alerts.com>

To: user@example.com

Subject: Immediate Action Required: Suspicious Sign-in Detected

Message-ID: suspicious-id@google-alerts.com

Authentication: All failed – high risk

⚠️ Key Phishing Indicators
Indicator	Details	Status
Spoofed Email	security@google-alerts.com not from real Google domain	❌
Malicious Source IP	Sent from 203.0.113.55 (unauthorized server)	❌
SPF/DKIM/DMARC	All authentication methods failed	❌
Threatening Subject	“Suspicious Sign-in Detected” to induce fear	⚠️
Generic Recipient	Sent to user@example.com (not personalized)	⚠️

🔍 Tool Used
Google Admin Toolbox – Message Header Analyzer
🔗 https://toolbox.googleapps.com/apps/messageheader/

📝 Conclusion
The analyzed email header strongly suggests a phishing attempt based on:

Sender domain spoofing

Failed SPF, DKIM, and DMARC checks

Misleading subject line

Originating from an untrusted IP

Such emails should be treated as malicious and reported or deleted immediately.

📁 Repo Structure
css
Copy
Edit
Phishing-Email-Analysis-Task2/
├── README.md
├── phishing_sample.txt
├── email_header_sample.txt
├── Messageheader.png
├── Message header analysis.png
└── Phishing_Email_Header_Analysis_Report.pdf
