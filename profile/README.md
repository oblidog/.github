# Findog

**A small, self-hosted ecosystem for keeping recurring payments and household obligations under control.**

Findog is built around a simple idea: bills and recurring costs should be easy to track, automate, and integrate without handing your financial workflow to another cloud service.

The project is currently in active development. The core ledger already handles recurring obligations, categories, payment state, and shared access; integrations and automation are being developed around a dedicated API client.

## Projects

| Repository | Purpose |
| --- | --- |
| [findog-ledger](https://github.com/findog-app/findog-ledger) | Main web application and API for managing ledgers, categories, and payment obligations. |
| [findog-client-python](https://github.com/findog-app/findog-client-python) | Python client for building external Findog integrations and automation. |
| [findog-legacy-core](https://github.com/findog-app/findog-legacy-core) | Legacy Findog core kept for the migration path to the new architecture. |

## Direction

Findog is moving toward a modular architecture:

- **Ledger** owns the financial domain and data.
- **API clients** provide a stable integration boundary.
- **Integrations** collect data from external providers independently of the main application.
- **Automation** handles recurring jobs such as obligation creation, invoice discovery, and payment updates.
- **Self-hosting first** keeps deployment and data ownership under the user's control.

## Status

🚧 **Early development** — APIs, data models, and UX may still change while the architecture settles.

The goal is not to become another accounting suite. Findog is deliberately focused on answering a much smaller question: **what needs to be paid, when, how much, and has it already been handled?**
