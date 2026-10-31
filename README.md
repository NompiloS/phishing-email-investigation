# SOC Phishing Email Investigation

## 1. Project Overview

This project demonstrates a simulated Security Operations Centre (SOC) investigation of a suspected phishing email.

The investigation focuses on identifying phishing indicators, assessing email security risks, outlining safe investigation procedures, and recommending appropriate incident response actions.

**Case Reference:** SOC-003  
**Incident Type:** Suspected Phishing  
**Environment:** Simulated SOC Investigation  
**Initial Verdict:** Likely Phishing

## 2. Incident Scenario

A user receives an email warning that their account may be suspended unless they take immediate action.

The message creates urgency and pressures the recipient to respond, potentially encouraging them to click a malicious link or disclose sensitive information.

As a SOC Analyst, the objective is to assess the email and determine whether it presents a phishing threat.

## 3. Identification of Suspicious Indicators

During the initial assessment, the following indicators were identified:

| Indicator | Observation | Risk |
|---|---|---|
| Urgent language | The email creates pressure to act immediately. | High |
| Account suspension threat | The recipient is warned they may lose account access. | High |
| Social engineering | The message may manipulate the recipient into taking action. | Medium |

These characteristics are commonly associated with phishing and social engineering attempts.

## 4. Investigation Methodology

The following steps outline the investigation process a SOC Analyst would follow.

### Step 1: Sender Analysis

- Review the sender's display name and email address.
- Verify whether the sending domain belongs to the organisation it claims to represent.
- Identify suspicious domains, misspellings, or impersonation attempts.
- Compare the sender address with known legitimate communication channels.

### Step 2: Email Header Analysis

Inspect the available email headers to identify inconsistencies and possible spoofing.

Key fields and authentication mechanisms include:

- **From:** The displayed sender address.
- **Return-Path:** The address used for email delivery and bounce handling.
- **Received:** The mail servers through which the message travelled.
- **SPF:** Checks whether the sending server is authorised for the domain.
- **DKIM:** Verifies the email's cryptographic signature.
- **DMARC:** Defines how receiving systems should handle messages that fail authentication alignment.

### Step 3: URL Analysis

- Inspect hyperlinks without opening them.
- Identify suspicious or misleading domains.
- Check for URL redirects and unusual characters.
- Assess suspicious URLs using approved security tools such as VirusTotal or Microsoft Defender.

### Step 4: Attachment Analysis

- Identify unexpected attachments.
- Review file names and extensions.
- Check available file metadata and hashes.
- Use approved malware analysis or sandboxing tools where available.
- Never open suspicious attachments on a production workstation.

## 5. Investigation Findings

| Investigation Area | Finding |
|---|---|
| Urgent language | Suspicious |
| Account suspension threat | Suspicious |
| Sender authenticity | Pending verification |
| Email headers | Not yet analysed |
| URL reputation | Not yet analysed |
| Attachments | Not yet analysed |

**Evidence limitation:** The simulated scenario did not include the original email, sender details, headers, URLs, or attachments. These areas would require further investigation before a definitive verdict could be reached.

## 6. Analyst Assessment

**Initial Verdict: Likely Phishing**

The urgent language and threat of account suspension indicate possible social engineering.

However, these indicators alone do not confirm that the email is malicious. Further analysis of the sender, authentication results, URLs, and attachments is necessary.

## 7. Recommended Incident Response Actions

If the email is confirmed as malicious, the SOC Analyst should:

1. Escalate the incident according to the organisation's incident response procedures.
2. Quarantine or remove the phishing email from affected mailboxes.
3. Identify other users who may have received the same email.
4. Block confirmed malicious URLs, domains, and sender addresses where appropriate.
5. If credentials were submitted, initiate a password reset and revoke active sessions.
6. Review authentication logs for suspicious sign-ins.
7. Document the investigation findings and remediation actions.

## 8. Tools and Technologies

The following tools can support phishing investigations:

- Microsoft Defender for Office 365
- Microsoft Defender XDR
- Microsoft 365 Exchange Admin Center
- VirusTotal
- Email header analysis tools
- DMARC analysis tools

These are relevant tools for the investigation workflow; they were not all used in this simulated case.

## 9. Skills Demonstrated

- Phishing email identification
- Email security investigation
- Email header analysis
- URL and attachment analysis
- Threat assessment and incident classification
- Social engineering detection
- Incident response and escalation
- SOC investigation documentation

## 10. References
- [Microsoft Learn – Investigate email threats](https://learn.microsoft.com/en-us/defender-office-365/investigate-email)
- [VirusTotal](https://www.virustotal.com/)
- [Microsoft Defender XDR](https://learn.microsoft.com/en-us/defender-xdr/)

**Disclaimer:** This project is based on a simulated phishing investigation for educational and portfolio purposes. No real user accounts, organisations, or sensitive information were involved.
