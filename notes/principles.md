# Notes: Security Principles

Quick reference on the core principles from Workbook 1, Module 05

- **Least Privilege** — give every user/system only the access they need, nothing more.
- **Defense in Depth** — layer multiple defenses so one failure doesn't mean total compromise.
- **Zero Trust** — never automatically trust a device or user, even inside the network; verify every request.
- **Authentication** — proving you are who you claim to be (e.g. a password).
- **Authorization** — deciding what an authenticated user is allowed to do.
- **Multi-Factor Authentication (MFA)** — requiring two or more independent proofs of identity.
- **Risk Management** — identifying what could go wrong, how likely and how bad it would be, and deciding what to do about it.

## The CIA Triad
- **Confidentiality** — only the right people can see the data.
- **Integrity** — data hasn't been changed without permission.
- **Availability** — data/systems are there when the right people need them.

## Why this matters for the risk assessment
The CIA Triad classification table in `final-project/risk-assessment.md` uses exactly these three categories to describe what each threat actually endangers — it's the same framework used throughout the risk register and mitigations.
