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


## Developer Certificate of Origin

Contributions are accepted under the same `GPL-2.0-or-later` license used by
the project. By contributing, you certify that you have the right to submit
the work under that license and agree to the Developer Certificate of Origin
1.1 in [DCO.md](DCO.md).

Every commit in a pull request must include a sign-off created with
`git commit --signoff`. The resulting commit message must contain a
`Signed-off-by: Name <email>` line matching the contributor. The sign-off
records provenance; it does not transfer copyright ownership to the maintainer.

Do not submit employer-owned, client-confidential, copied or AI-generated
material unless you have verified that it may lawfully be distributed under
the project license. Clearly identify third-party material and its license.

New original source files should include
`SPDX-License-Identifier: GPL-2.0-or-later` in the appropriate comment
syntax.
