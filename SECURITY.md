# Security Policy

## Supported versions

Security fixes are provided for the latest public beta. Older beta builds are retained for traceability but are not supported.

| Version | Supported |
|---|---|
| 0.2-beta | Yes |
| 0.1.x-beta | No |

## Reporting a vulnerability

Use GitHub Private Vulnerability Reporting in the repository Security tab. Do not disclose suspected vulnerabilities, credentials, personal data, session material or production URLs in a public issue.

Include the affected version, GLPI and PHP versions, reproduction steps, expected impact and the smallest evidence needed to validate the report. Remove or mask personal and institutional data.

We aim to acknowledge a report within five business days. Triage and remediation time depend on severity, GLPI compatibility and the need for coordinated disclosure.

## Scope

Relevant boundaries include GLPI authentication and session reuse, ACL by profile/entity/item, CSRF, uploads, chatbot write actions, delegated forms, personal data, voice assets and browser-side accessibility controls.

Good-faith research that avoids privacy violations, service disruption and persistence is welcome.
