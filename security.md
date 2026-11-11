---
layout: page
title: Security policy
permalink: /security/
---

_Last updated: 11 November 2026_

This policy applies to the Atlassian Marketplace app **Dashboard Statistics – Team, Organization & Sums for Jira** (the "App"), provided by **Bc. Tomáš Buchta, sole trader, Company ID (IČO) 21540951, Ostrava, Czech Republic** ("we").

## Reporting a vulnerability
Send security issues to **[security@tsutsei-support.atlassian.net](mailto:security@tsutsei-support.atlassian.net)**. Every message creates a tracked request in our support system. Please include the app, your site URL, steps to reproduce and the impact you expect. Do not include passwords, API tokens or customer data.

We confirm receipt within 2 business days, keep you informed about the fix and credit you in the release notes if you wish. Please give us reasonable time to release a fix before disclosing the issue publicly.

## Architecture
- The App runs entirely on **Atlassian Forge** ("Runs on Atlassian") as Custom UI served by Atlassian. It has **no server-side code**: no Forge functions, no Forge Remote, no egress to external servers, no vendor-side servers.
- The App **stores nothing**. The settings of a gadget (filter id and name or JQL, chosen fields, display options) are kept by Jira as properties of the dashboard, under Jira's own permissions.
- Work items are read in the user's browser with the signed-in user's permissions, so everyone sees only statistics of work items Jira shows them. The vendor never receives any customer data.
- The App requests a single read-only scope (`read:jira-work`) and never asks for passwords or API tokens. It cannot change anything in Jira.
- The App does not use AI or machine-learning models, and no customer data is processed by such models.

## Secure development
- Gadget settings are validated every time they are read (field ids, filter ids, enumerated options, limits), because Jira stores what a dashboard editor submitted.
- All text – field names, values, filter names, titles – is added to the page as text, never as HTML. JQL typed by a user runs only as that user's own search. Downloaded CSV files are guarded against spreadsheet formula injection.
- The App writes no logs.
- Every change passes automated unit and end-to-end tests (statistics compared with the Jira search for every field type) before it is deployed to production.
- Dependencies are checked with `npm audit` before every release; known vulnerabilities are fixed before deploying.

## Access control
- Source code is in private GitHub repositories; GitHub and Atlassian accounts are protected with two-factor authentication.
- The developer workstation uses full-disk encryption, automatic operating system and security updates, a firewall and malware protection. Unsupported operating system versions are not used.
- Access to source code, the Forge developer console, the Marketplace partner account and the support site is reviewed every quarter.

## Fixing vulnerabilities
Vulnerabilities are scored with CVSS and fixed within the deadlines of the Atlassian Marketplace security bug fix policy:

| Severity | CVSS | Fix released within |
|---|---|---|
| Critical | 9.0 – 10.0 | 10 days |
| High | 7.0 – 8.9 | 4 weeks |
| Medium | 4.0 – 6.9 | 12 weeks |
| Low | 0.1 – 3.9 | 25 weeks |

Forge deployments reach all installations within minutes, so customers do not need to update the App.

## Security incidents
If a security incident may affect customer data, we report it to Atlassian within 24 hours and notify the admins of affected sites within 72 hours where possible. As a data processor under the GDPR, we inform controllers without undue delay. See also the [privacy policy]({{ '/privacy/' | relative_url }}) and the [Data Processing Addendum]({{ '/dpa/' | relative_url }}).
