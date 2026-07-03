# Airbase (airbase)

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
