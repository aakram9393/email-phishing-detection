# Threat Model – Email Phishing Detection System

## 1. Objective
The objective of this system is to detect phishing emails based on their
textual content and basic metadata using machine learning techniques.
The system aims to classify emails as either phishing or legitimate
with an explainable risk score.

## 2. Assets to Protect
- User credentials (usernames and passwords)
- Corporate email users
- Brand reputation of impersonated services


## 3. Threat Actors
- Cybercriminals sending mass phishing campaigns
- Attackers impersonating well-known brands
- Opportunistic attackers using generic phishing templates

## 4. Attacks In Scope
- Credential harvesting emails
- Fake account verification or password reset emails
- Emails containing suspicious links
- Brand impersonation using social engineering language
Examples:

“Your account will be locked”

“Verify your identity”

“Suspicious login detected”

## 5. Attacks Out of Scope
- Malware attachments (PDF, ZIP, EXE)
- Image-only phishing emails
- Highly targeted spear-phishing
- Zero-day phishing techniques

## 6. Assumptions
- Email body and subject are available for analysis
- Labels in the dataset are reasonably accurate
- Attack patterns in historical data resemble current attacks

## 7. Risks & Limitations
- Attackers may adapt language to evade detection
- Dataset may be biased or outdated
- Model may produce false positives on legitimate emails

