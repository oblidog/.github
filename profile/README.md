# Oblidog

**A self-hosted system for keeping recurring payments and household obligations under control.**

Oblidog answers four practical questions: **what needs to be paid, when, how much, and has it already been handled?**

The project combines a central ledger with a stable Python SDK and independently deployed provider integrations. It is designed for people who want useful automation without handing their financial workflow and data to another hosted service.

## Projects

| Repository | Purpose |
| --- | --- |
| [oblidog-ledger](https://github.com/oblidog/oblidog-ledger) | Main web application and API for obligations, categories, payment state, reports, and automation. |
| [oblidog-client-python](https://github.com/oblidog/oblidog-client-python) | Supported Python SDK for the Oblidog integration API. |
| [oblidog-integrations](https://github.com/oblidog/oblidog-integrations) | Independently deployed integrations that collect data from external providers. |
| [findog-legacy-core](https://github.com/oblidog/findog-legacy-core) | Legacy compatibility adapter retained only for migration from the original Findog workbook. |

## Architecture

- **Ledger** owns the financial domain and data.
- **Client** provides the supported integration boundary.
- **Integrations** communicate with external providers without coupling them to the main application.
- **Automation** runs recurring jobs such as obligation creation, invoice discovery, and payment updates.
- **Self-hosting first** keeps deployment and data ownership under the user's control.

## Status

🚧 **Active development** — the core workflow is operational, while integrations, documentation, and public package distribution are still evolving.

## Migrating existing clones

GitHub redirects old repository URLs, but active clones should use the canonical remotes:

```bash
git remote set-url origin https://github.com/oblidog/oblidog-ledger.git
# or:
git remote set-url origin https://github.com/oblidog/oblidog-client-python.git
git remote set-url origin https://github.com/oblidog/oblidog-integrations.git
```

Use the command matching the repository in the current clone.
