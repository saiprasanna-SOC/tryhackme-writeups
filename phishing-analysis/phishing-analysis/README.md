# TryHackMe — Phishing Analysis

## Overview

This lab provided hands-on practice investigating phishing emails and identifying indicators that can be used to determine whether an email is malicious.

The investigation focused on email analysis, authentication mechanisms, malicious links and attachments, threat intelligence, and network traffic.

---

## Objectives

* Understand phishing attacks and common techniques
* Analyze suspicious email headers
* Investigate email sender information
* Examine URLs and attachments
* Identify Indicators of Compromise (IOCs)
* Understand SPF, DKIM, and DMARC
* Investigate Business Email Compromise (BEC)
* Use threat intelligence platforms
* Analyze SMTP traffic using Wireshark
* Document investigation findings

---

## Topics Covered

### Phishing Fundamentals

Learned how attackers use social engineering techniques to convince victims to:

* Click malicious links
* Open malicious attachments
* Provide credentials
* Transfer money
* Reveal sensitive information

---

### Email Header Analysis

Investigated email headers to understand:

* Sender and recipient information
* Mail server routing
* Source IP addresses
* Authentication results
* Suspicious email characteristics

Email headers can provide valuable evidence during phishing investigations.

---

### SPF, DKIM & DMARC

Practiced analyzing email authentication results.

**SPF**

Helps determine whether a mail server is authorized to send email for a domain.

**DKIM**

Provides cryptographic verification that an email was authorized by the sending domain and was not improperly modified.

**DMARC**

Allows domain owners to define how receiving systems should handle messages that fail authentication.

I practiced interpreting authentication results such as:

* SPF Pass
* SPF SoftFail
* DKIM results
* DMARC results
* DMARC `p=reject` policies

---

## URL Investigation

Suspicious URLs were investigated using threat intelligence and analysis tools.

The investigation process included:

1. Extracting the URL
2. Identifying the domain
3. Checking reputation
4. Searching for known malicious activity
5. Reviewing available analysis results
6. Determining whether the URL should be considered suspicious or malicious

---

## Attachment Investigation

Suspicious email attachments were examined as potential sources of malicious activity.

The investigation included:

1. Identifying the attachment
2. Calculating the file hash
3. Searching the hash using threat intelligence
4. Checking for known malicious activity
5. Documenting the findings

Example:

```bash
sha256sum filename
```

The resulting SHA-256 hash can be used as an IOC for further investigation.

---

## Business Email Compromise (BEC)

The lab also covered Business Email Compromise, where attackers use impersonation or compromised accounts to perform fraudulent activities.

Examples include:

* Executive impersonation
* Vendor impersonation
* Fake payment requests
* Credential theft
* Account compromise

---

## Network Traffic Analysis

Used **Wireshark** to investigate email-related network traffic.

Protocols and concepts included:

* SMTP
* DNS
* IMAP

Wireshark filters can help isolate relevant traffic and identify suspicious communication.

---

## Tools Used

| Tool        | Purpose                                    |
| ----------- | ------------------------------------------ |
| Thunderbird | Email and message-source analysis          |
| CyberChef   | Data decoding and transformation           |
| VirusTotal  | File, URL, and domain intelligence         |
| ANY.RUN     | Sandbox analysis                           |
| Cisco Talos | Threat intelligence                        |
| Wireshark   | Network traffic analysis                   |
| SHA-256     | File identification and integrity checking |

---

## Investigation Workflow

```text
Suspicious Email
      ↓
Initial Triage
      ↓
Analyze Email Headers
      ↓
Inspect URLs / Attachments
      ↓
Check SPF / DKIM / DMARC
      ↓
Threat Intelligence Investigation
      ↓
Network Traffic Analysis
      ↓
Identify IOCs
      ↓
Determine Severity
      ↓
Document Findings
```

---

## Indicators of Compromise

Potential IOCs identified during phishing investigations include:

* Malicious email addresses
* Suspicious domains
* Malicious URLs
* IP addresses
* File hashes
* Suspicious attachments
* Abnormal email headers

---

## Key Takeaways

This lab helped me develop practical experience with:

* Phishing investigation
* Email header analysis
* Email authentication
* Threat intelligence
* URL investigation
* Attachment analysis
* IOC identification
* Network traffic analysis
* Security investigation documentation

It also helped me understand how different pieces of evidence can be combined to determine whether a suspicious email represents a potential security incident.

---

## Skills Demonstrated

**SOC Skills**

* Alert triage
* Evidence collection
* IOC identification
* Threat investigation
* Security documentation

**Technical Skills**

* Email analysis
* Wireshark
* Threat intelligence
* SPF / DKIM / DMARC
* Hash analysis
* Network protocol analysis

---

## Source

Training platform: **TryHackMe**

This documentation represents my own learning notes and investigation process rather than a reproduction of official lab answers.

---

## Disclaimer

This work was completed in an authorized cybersecurity training environment for educational purposes.

No real-world unauthorized systems, accounts, or confidential information were targeted.
