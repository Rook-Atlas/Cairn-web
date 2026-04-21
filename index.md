---
title: Cairn
layout: default
---

# Cairn

**Your money, marked out.**

Cairn is a self-hosted, privacy-first personal finance platform for
households. A built-in AI companion — **Ledger** — helps you understand
where you stand and what to do next.

> **Status:** In development. Private beta. Public release planned Q3 2026.

---

## The problem

Every existing personal finance app asks you to do one of three things:

1. **Hand your bank credentials to a third party** that ultimately routes
   through services you don't control
2. **Pay a monthly subscription** for a product you never actually own —
   if they shut down or pivot, your budget history goes with them
3. **Sell you something** — investment products, credit cards, loans,
   advertising, or your aggregated behavior data

Cairn rejects all three.

---

## The Cairn model

- **You own the data.** Everything lives as JSON on your machine.
- **You own the runtime.** Host Cairn on your own hardware.
- **AI where it actually helps.** Ledger, the built-in companion, answers
  questions grounded in **your own data**. No per-query API fees.
- **Optional live bank sync.** Connect an aggregator for real-time
  transactions, or stay fully offline with CSV imports.
- **Built for households.** Multiple accounts, shared goals, shared
  timelines, with privacy controls between members.
- **Honest by design.** No false "safe to spend" numbers, no upsell
  funnels, no engagement hacks.

---

## What Cairn does

- **Traffic-light status** — stable / tight / short at a glance
- **45-day payment timeline** — every upcoming debit and credit
- **Past-due catch-up tracker** — one-time dig-out amounts ranked by
  real consequence
- **Levers view** — income opportunities you haven't pulled yet
- **Lumpy-expense planner** — sinking funds for irregular costs
- **CSV import** for most US banks — works fully offline
- **Gmail receipt parsing** (opt-in) for automatic bill ingestion
- **Subscription detection** from your real transactions

---

## Who it's for

- Privacy-minded people who don't want their transaction data in
  third-party analytics pipelines
- Households that need shared budgeting without exposing every detail
- Developers and technically inclined users comfortable running a
  local service
- Anyone burned by a finance app that shut down, got acquired, or
  changed its pricing

---

## Security model

- Local-only by default
- PBKDF2-SHA256 passwords, HMAC-signed session cookies
- **Read-only integrations only.** Cairn cannot move money, initiate
  transfers, or execute trades on your behalf
- Your password is the only wall when exposed remotely — choose a
  strong one

---

## Planned integrations

- [x] CSV import (Discover, Capital One, Chase, Ally, Best Buy Citi)
- [x] Gmail receipt ingestion
- [ ] Plaid (transaction sync + balances) — in review
- [ ] Teller.io aggregator
- [ ] SimpleFIN Bridge
- [ ] Native email-alert parsing (no aggregator required)

---

## License

Copyright (c) 2026 Wesley Carpenter (d/b/a Rook Atlas). All rights reserved.

Cairn is proprietary software. Source is not publicly available during
private beta. An open-core release model is being evaluated for public
release.

---

## Contact

**Questions, beta access, partnership inquiries:**
[w.carpenter226@gmail.com](mailto:w.carpenter226@gmail.com)

Follow the [repository](https://github.com/Rook-Atlas/Cairn-web) for
release announcements.
