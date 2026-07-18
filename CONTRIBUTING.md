# Contributing

## Development requirements

- PHP 8.1 or later;
- Composer 2;
- Node.js 20 or later for accessibility tooling;
- gettext/msgfmt for translation validation;
- a GLPI 10 or GLPI 11 test environment for integration work.

## Quality checks

Run before opening a pull request:

```text
composer install
composer qa
pwsh -File tools/compile-locales.ps1
pwsh -File tools/i18n-audit.ps1 -RequireMsgfmt
npm ci
```

Changes to UI or workflows must also cover keyboard operation, visible focus, reflow/zoom, high contrast/forced colors and screen-reader semantics. Changes to tickets, forms, KB or chatbot actions must preserve GLPI profile, entity, ACL and CSRF checks.

Never commit credentials, authenticated browser sessions, production URLs, personal data, generated release folders, dependency directories or local audit reports.

Keep changes scoped, document compatibility assumptions and add regression tests for security- or permission-sensitive behavior.
