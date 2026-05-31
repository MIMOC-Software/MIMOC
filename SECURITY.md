# Security Policy

## Reporting a vulnerability

Please do not report security vulnerabilities through public GitHub issues.

If you believe you have found a security issue in MIMOC, open a generic issue stating that you would like to report a security concern. Do not include technical exploit details, credentials, logs, screenshots or sensitive data in the public issue.

A private communication channel will be arranged for the technical details.

## What to include in a private report

When reporting a vulnerability privately, include as much of the following as possible:

- affected MIMOC version;
- operating system and deployment type;
- affected module or feature;
- steps to reproduce;
- expected behavior;
- actual behavior;
- potential impact;
- whether the issue requires authentication;
- whether administrative privileges are required;
- sanitized logs or screenshots, if relevant.

Do not include real credentials, private keys, license signing keys, production databases or unredacted sensitive data.

## Supported versions

During the Community / Early Access phase, only the latest published build is considered supported for security review and fixes.

Older builds may be superseded without backported fixes.

## Scope

Security reports may include issues related to:

- authentication and authorization;
- local user management;
- role-based access control;
- credential vault handling;
- audit integrity;
- database protection;
- license handling;
- unsafe deployment behavior;
- unintended privilege escalation;
- sensitive data exposure;
- insecure defaults;
- tamper or integrity checks.

## Out of scope

The following are generally out of scope unless they demonstrate a direct MIMOC vulnerability:

- attacks requiring full compromise of the operating system;
- keyloggers, malware or memory scraping already running as administrator;
- social engineering;
- denial-of-service against third-party infrastructure;
- vulnerabilities in unsupported or obsolete operating systems;
- issues caused by deliberate misconfiguration outside documented guidance.

## Responsible disclosure

Please allow reasonable time for investigation and remediation before disclosing vulnerability details publicly.

## Sensitive operational data

MIMOC can process infrastructure data such as hostnames, IP addresses, MAC addresses, installed software, audit events, job history and credential references.

When discussing support or security issues, sanitize all data that could reveal internal infrastructure or confidential information.
