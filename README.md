## Hello there — I'm Albert Tseng 👋

Backend engineer in Taipei, working on cross-border payments and crypto-fiat rails.
I like systems where being wrong costs money — ledgers, idempotency, reconciliation.

📮 [tjtseng1072@gmail.com](mailto:tjtseng1072@gmail.com)

<!-- ─────────────────────────────────────────────────────────────
     SKELETON — uncomment each section as you fill it in.
     Everything below is hidden from the rendered profile page.
     ───────────────────────────────────────────────────────────── -->

<!--
### Currently

- Building payment infrastructure at **XREX** — TODO: one line, with a number
- **Open to backend / payments roles in Australia** — Melbourne or Sydney, on-site or remote
- Work rights: TODO (482 sponsorship / 189 / 190 / WHV / PR)
- Timezone: UTC+8, ~2–3h from AEST — near-full overlap with an Australian workday
-->

<!--
### What I'm building

#### [LedgerPay](https://github.com/TJ72/ledgerpay) — a Stripe-shaped payment platform, built to be correct

Merchants integrate a REST API, customers pay through a hosted checkout, and every
money movement lands in a balanced double-entry ledger.

Deliberately a **modular monolith first** — each module owns its tables and exposes a
Go API, so extracting `ledger-service` later is a mechanical move, not a redesign.

```mermaid
flowchart LR
    shop["demo-shop<br/>(merchant storefront)"] -->|REST + webhooks| api
    checkout["web/checkout<br/>(hosted checkout page)"] -->|REST| api

    subgraph api["backend — single Go binary"]
        merchant["merchant<br/>API keys, auth"]
        payment["payment<br/>payment intents,<br/>checkout sessions"]
        ledger["ledger<br/>double-entry core"]
        payment --> ledger
        payment --> merchant
    end

    api --> pg[("PostgreSQL")]
```

Go 1.25 · PostgreSQL 16 · Next.js
-->

<!--
### Why Australia

TODO — the domain-knowledge hook. Connect XREX crypto-fiat / AML experience to
the Australian payments stack: NPP / PayTo, BECS Direct Debit, Osko, AUSTRAC,
CDR. Two or three sentences, no more.
-->

<!--
### Tech

**Reach for daily** — Go, PostgreSQL, TypeScript, Docker
**Comfortable in** — Next.js, Kubernetes, Terraform, GitHub Actions
**Currently learning** — TODO
-->

<!--
### Writing

TODO — link the single best post directly, not the blog index, until there are 4–5.
-->

<!--
### Fun fact

TODO — something concrete and true that a stranger could open a conversation with.
Not "I like coffee."
-->
