# Security Policy

This document covers the **organization-wide vulnerability reporting process** for every `flowwarden-io` repository. Individual projects may define their own `SECURITY.md` to declare which versions are supported and to override any of the points below.

## Reporting a Vulnerability

We take the security of FlowWarden projects seriously. If you believe you have found a security vulnerability, please report it responsibly through one of the following channels.

**Please do NOT open a public GitHub issue for security vulnerabilities.**

### Preferred: GitHub Security Advisories

Use the **"Report a vulnerability"** button on the **Security** tab of the affected repository to open a private security advisory. This channel allows us to coordinate the fix privately before public disclosure and to request a CVE if appropriate.

### Alternative: Email

If you prefer not to use GitHub Security Advisories, send a report to:

**security@flowwarden.io**

Please encrypt sensitive details if possible.

### What to include in your report

- The repository / project affected
- A clear description of the vulnerability
- Steps to reproduce (or a proof-of-concept if available)
- The affected version(s)
- The potential impact (data exposure, code execution, denial of service, etc.)
- Any suggested mitigation or fix, if known

## Response Timeline

We aim to respond to security reports according to the following timeline:

| Stage                | Target time      |
| -------------------- | ---------------- |
| Acknowledgement      | Within 72 hours  |
| Initial assessment   | Within 7 days    |
| Fix and disclosure   | Depends on severity, in coordination with the reporter |

These are best-effort targets — FlowWarden projects are maintained as side projects. Critical vulnerabilities will be prioritized.

## Disclosure Policy

We follow a **coordinated disclosure** model:

- Vulnerabilities are kept private until a fix is available.
- We will work with the reporter to agree on a disclosure timeline (typically 30 to 90 days, shorter for actively exploited issues).
- Once a fix is released, we publish a security advisory describing the vulnerability, the fix, and credit the reporter (unless they prefer to remain anonymous).

## Out of Scope (generic)

The following are generally not considered security vulnerabilities in FlowWarden libraries themselves:

- Issues in user code that misuses a library (e.g., handlers that do not validate input)
- Vulnerabilities in dependencies that have already been disclosed and have published fixes — please report those upstream
- Configuration issues in user deployments (insufficient authentication, exposed credentials, etc.)

Individual projects may extend this list in their per-repo `SECURITY.md`.

Thank you for helping keep the FlowWarden ecosystem and its users safe.
