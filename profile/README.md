<p align="center">
  <a href="https://oblidog.com">
    <img src="https://raw.githubusercontent.com/oblidog/oblidog-ledger/main/frontend/public/assets/images/oblidog-logo.svg" alt="Oblidog" width="280">
  </a>
</p>

<h2 align="center">Keep your payments on a leash.</h2>

<p align="center">
  A self-hosted home for recurring bills and household obligations.<br>
  Know what is due, automate what you can, and keep the history.
</p>

<p align="center">
  <a href="https://oblidog.com">Website</a> ·
  <a href="https://demo.oblidog.com">Try the demo</a> ·
  <a href="https://github.com/oblidog/oblidog-ledger/blob/main/docs/self-hosting.md">Self-hosting guide</a>
</p>

Bills arrive in different provider portals, amounts change every month, and
payment status is easy to lose track of. Oblidog brings that work into one
place—from collecting the bill details to marking it paid and comparing it
with previous periods.

## What you can do

- **See what needs attention.** Review upcoming, overdue, incomplete,
  ready-to-pay, and paid obligations.
- **Keep the details.** Track amounts, due dates, charge components,
  readings, and structured provider data across billing periods.
- **Automate recurring work.** Import provider data and recognize payment
  status with separately deployed integrations, or enter details manually.
- **Share the work.** Use shared ledgers with owner, editor, and viewer roles.
- **Own the data.** Run the application on your own infrastructure.

Oblidog tracks bills and payment status; it does not initiate bank payments.

## Projects

| Repository | Purpose |
| --- | --- |
| [oblidog-ledger](https://github.com/oblidog/oblidog-ledger) | Web application and API for recurring obligations, shared ledgers, history, and reports. Start here to self-host Oblidog. |
| [oblidog-client-python](https://github.com/oblidog/oblidog-client-python) | Python SDK for building integrations against the Ledger integration API. Published on PyPI as `oblidog-client`. |
| [oblidog-integrations](https://github.com/oblidog/oblidog-integrations) | Provider adapters for e-Kartoteka, iPrzedszkole, and NJU Mobile, deployed as scheduled one-shot jobs. |
| [oblidog-website](https://github.com/oblidog/oblidog-website) | Public landing page at [oblidog.com](https://oblidog.com). |

## How automation fits together

**Ledger** owns the obligations and their history. Its built-in System Run
creates obligations, estimates missing amounts, and sends reports when email
is configured.

**Provider integrations** run separately on your chosen schedule. They use the
Python SDK and a key scoped to one integration and category to synchronize
amounts, bill components, provider data, and payment status. System Run does
not launch these external jobs.

Use the existing adapters or build one for your own provider:

- [Integration API guide](https://github.com/oblidog/oblidog-ledger/blob/main/docs/integration-api.md)
- [Python SDK documentation](https://oblidog.github.io/oblidog-client-python/)
- [Integration deployment guide](https://github.com/oblidog/oblidog-integrations#host-deployment)

## Project status

Oblidog is open-source software in active early development. The core bill
workflow, shared ledgers, historical views, integration API, and self-hosting
setup are available. Interfaces and provider coverage continue to evolve.

To report a bug or suggest an improvement, open an issue in the relevant
repository. For application setup, start with the
[Ledger README](https://github.com/oblidog/oblidog-ledger#readme) and
[self-hosting guide](https://github.com/oblidog/oblidog-ledger/blob/main/docs/self-hosting.md).
