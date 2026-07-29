# Personal Cybersecurity Risk Assessment & Awareness Guide

*Final Project — Workbook 1: Introduction to Cybersecurity*

## Subject

**Beacon Retail Co.** — a fictional 12-employee retail store with an online shop, used as a stand-in subject so the assessment can be published publicly without exposing any real data.

## Executive Summary

"This report reviews the main digital assets used by Beacon Retail Co. — customer payment data, email accounts, point-of-sale systems, and the company website — and identifies the most realistic threats to each. The biggest risks are phishing attacks against employee email and a possible breach of customer payment data, both of which could cause serious financial and reputational damage. The recommended next steps are enabling multi-factor authentication everywhere, keeping software patched, and training staff to recognize phishing attempts."

## 1. Assets Identified

| # | Asset | Type |
|---|-------|------|
| 1 | Customer payment data | Data |
| 2 | Employee email accounts | Account |
| 3 | Point-of-sale (POS) terminals | Device |
| 4 | Company Wi-Fi network | Infrastructure |
| 5 | Customer database (CRM) | Data |
| 6 | Admin/owner accounts | Account |

## 2. Threats & CIA Triad Classification

| Asset | Realistic Threat | Confidentiality | Integrity | Availability |
|-------|-------------------|:---:|:---:|:---:|
| Customer payment data | Third-party vendor breach | ✔ | ✔ | – |
| Employee email accounts | Phishing / credential theft | ✔ | – | – |
| POS terminals | Malware via unpatched software | ✔ | ✔ | ✔ |
| Company Wi-Fi | Unauthorized outside access | ✔ | – | – |
| Customer database (CRM) | Ransomware | – | ✔ | ✔ |
| Admin/owner accounts | Password reuse → account takeover | ✔ | ✔ | ✔ |

*(✔ marks which part of the CIA Triad is threatened. A ransomware attack, for example, doesn't necessarily expose data to outsiders (Confidentiality), but it does threaten Integrity and Availability.)*

## 3. Risk Register

See [`risk-register.csv`](./risk-register.csv) for the full table (Asset | Threat | Likelihood | Impact | Mitigation). Preview:

| Asset | Threat | Likelihood | Impact | Mitigation |
|-------|--------|:---:|:---:|-----|
| Customer payment data | Payment system breach via third-party vendor | Medium | High | Network segmentation; PCI-DSS compliant processor |
| Employee email accounts | Phishing leading to credential theft | High | Medium | Security awareness training; MFA on all accounts |
| POS terminals | Malware via unpatched software | Medium | High | Regular patch management; endpoint antivirus |
| Company Wi-Fi | Unauthorized outside access | Low | Medium | WPA3 encryption; guest network separated from internal |
| Customer database (CRM) | Ransomware | Medium | High | Offline/immutable backups; least-privilege DB access |
| Admin/owner accounts | Password reuse → account takeover | Medium | High | Password manager; mandatory MFA |

## 4. Security Basics Guide (one page, plain language)

**Authentication** — proving who you are, usually with a username and password. A weak or reused password is the easiest way in for an attacker, so every account should have a unique, strong password.

**Multi-Factor Authentication (MFA)** — a second proof of identity beyond the password (like a code from your phone). Even if a password is stolen or guessed, MFA stops it from being enough on its own — this single control would have prevented several of the real-world breaches studied in this workbook (including Colonial Pipeline).

**Phishing Awareness** — most attacks don't start with clever hacking; they start with a convincing email or message. Before clicking a link or entering credentials, check: does the sender's address actually match the real company? Is there artificial urgency? Is it asking for information it shouldn't need?

## 5. Recommended Tool

**Recommendation: Nessus (or OpenVAS for a free alternative)**

Justification: Beacon Retail Co.'s biggest exposure is unpatched software across POS terminals and servers. A vulnerability scanner run on a regular schedule would catch missing patches and misconfigurations before an attacker finds them — directly addressing the highest-impact risks in the register above (rows 1 and 3).

## 6. Executive Summary

---
*This is a training exercise built on a fictional company. No real personal or customer data is used.*
