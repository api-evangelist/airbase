# Airbase (airbase)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Airbase is a modern spend management platform for finance teams that combines accounts-payable (AP) automation and bill pay, guided procurement and purchase orders, corporate cards, and expense reimbursements on a single system with real-time general-ledger sync.

**Operating status / acquisition:** Airbase Inc. was acquired by **Paylocity** in a deal valued at approximately **$325M** - the definitive agreement was announced **September 4, 2024** and the acquisition **completed October 1, 2024**. Airbase now operates as **"Airbase by Paylocity,"** extending Paylocity's HCM suite into the office of the CFO. The product and its developer portal remain live.

**API access model (important):** Airbase exposes a developer platform at [developer.airbase.io](https://developer.airbase.io/) that documents a REST API, OpenAPI/Swagger definitions, Postman and Insomnia collections, a webhooks management API, an OAuth playground, authentication, and a sandbox. The API is **real but account-gated** - it is intended for Airbase customers building custom connections (notably ERP/GL) for systems not covered by the pre-built integrations, and credentials are provisioned inside the customer's Airbase/Paylocity tenant rather than through open self-serve public signup. Because the reference lives behind that gated, branded single-page portal, the logical APIs documented here are **honestly modeled** from the documented product surface (`endpointsModeled`); exact endpoint paths, the API base URL, and full OpenAPI are **not fabricated**.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/airbase/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/airbase/refs/heads/main/apis.yml)

## Tags

- Spend Management
- Accounts Payable
- Bill Pay
- Procurement
- Corporate Cards
- Expense Management
- FinTech
- Paylocity
- Gated API

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs (modeled from the documented product surface)

Each API below is honestly modeled from Airbase's documented spend-management product and developer portal. Endpoints are gated (`endpointsModeled`); exact paths are not reproduced.

### Airbase Bills & AP Automation API

Create, list, retrieve, and update bills and vendor invoices flowing through Airbase's AP automation - line items, approval state, payment status, and payment method.

- **Human URL:** [https://developer.airbase.io/](https://developer.airbase.io/)

### Airbase Purchase Requests & Orders API

Create and track guided purchase requests and purchase orders - intake details, line items, vendor and GL coding, budget checks, and the approval milestones a request transitions through (Airbase emits webhook events such as "purchase request approved").

- **Human URL:** [https://developer.airbase.io/](https://developer.airbase.io/)

### Airbase Vendors API

Manage the vendor/supplier master record - vendors, payment details, tax and onboarding information, and the relationships bills, POs, and payments are made against. Airbase also runs a separate vendor portal at [vendors.airbase.io](https://vendors.airbase.io/).

- **Human URL:** [https://developer.airbase.io/](https://developer.airbase.io/)

### Airbase Corporate Cards API

List corporate and virtual cards, card holders, spend limits and controls, and card policies to reconcile card spend against budgets and the general ledger.

- **Human URL:** [https://developer.airbase.io/](https://developer.airbase.io/)

### Airbase Transactions API

Pull unified transaction and spend data across cards, bills, and reimbursements - amounts, merchants, dates, GL coding, and reconciliation status - for reporting and close.

- **Human URL:** [https://developer.airbase.io/](https://developer.airbase.io/)

### Airbase Expense Reimbursements API

Create and track employee expense reimbursements and out-of-pocket claims - receipts, line items, approval state, and payout status.

- **Human URL:** [https://developer.airbase.io/](https://developer.airbase.io/)

### Airbase Approvals API

Inspect and act on the multi-step approval workflows that gate purchase requests, bills, cards, and reimbursements - approvers, policy rules, current state, and milestone transitions (also delivered as webhook events).

- **Human URL:** [https://developer.airbase.io/](https://developer.airbase.io/)

### Airbase GL & Accounting Sync API

Read and push general-ledger coding and accounting records so spend stays in sync with the ERP/GL. Airbase promotes a REST API specifically for building custom ERP/GL connections for systems not on its pre-built integration list.

- **Human URL:** [https://www.airbase.com/sheets/erp-integration-api](https://www.airbase.com/sheets/erp-integration-api)

### Airbase Webhooks Management API

Register and manage webhook subscriptions so external systems receive Airbase events (e.g. a purchase request approved or a workflow milestone transition) as JSON payloads (`id`, `object`, `type`, `created_date`, `data`).

- **Human URL:** [https://developer.airbase.io/](https://developer.airbase.io/)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/airbase)
- [Website](https://www.airbase.com/)
- [Documentation](https://developer.airbase.io/)
- [Plans](plans/airbase-plans-pricing.yml)
- [Rate Limits](rate-limits/airbase-rate-limits.yml)
- [Fin Ops](finops/airbase-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
