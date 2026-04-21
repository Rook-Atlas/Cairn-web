# Cairn

**Your money, marked out.**

Cairn is a self-hosted, privacy-first personal finance platform for
households. A built-in AI companion — **Ledger** — helps you understand
where you stand and what to do next.

> **Status:** In development. Private beta. Public release planned Q3 2026.

---

## The problem

Every existing personal finance app asks you to do one of three things:

1. **Hand your bank credentials to a third party** (Plaid, MX, Finicity)
   that ultimately routes through services you don't control
2. **Pay a monthly subscription** for a product you never actually own —
   if they shut down or pivot, your budget history goes with them
3. **Sell you something** — investment products, credit cards, loans,
   advertising, or your aggregated behavior data

Cairn rejects all three.

---

## The Cairn model

- **You own the data.** Everything lives as JSON on your machine. No
  database dependency, no cloud lock-in, no vendor can go dark on you.
- **You own the runtime.** Host Cairn on your own hardware — a laptop, a
  Raspberry Pi, a home server, or a private VPS. Your choice.
- **AI where it actually helps.** Ledger, the built-in companion, answers
  questions grounded in **your own data**. Uses your existing Claude
  subscription via the Agent SDK. No per-query API fees.
- **Optional live bank sync.** Connect Plaid or a similar aggregator for
  real-time transaction imports, but the CSV path always works — fully
  offline.
- **Built for households.** Multiple accounts, shared goals, shared
  timelines, with privacy controls between members.
- **Honest by design.** The dashboard tells you the truth — no false
  "safe to spend" numbers, no upsell funnels, no engagement hacks.

---

## What Cairn does

- **Traffic-light status** — stable / tight / short, at a glance, without
  scary dollar numbers that spiral your partner
- **45-day payment timeline** — every upcoming debit and credit, sorted
  by date and urgency, with running cash delta
- **Past-due catch-up tracker** — one-time dig-out amounts ranked by
  real consequence (disconnects, credit reporting, late fees)
- **Levers view** — income opportunities you haven't pulled yet
  (tax withholding, HRA reimbursements, loan optimization)
- **Lumpy-expense planner** — sinking funds for inspections, vet bills,
  quarterly surprises
- **CSV import** for Discover, Capital One, Chase, Ally, and most US
  banks — works without any aggregator
- **Gmail receipt parsing** (opt-in OAuth) for automatic bill ingestion
- **Subscription detection** from your real transaction stream

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

## Under the hood

- Self-hosted Windows service (Linux/Mac support planned)
- PowerShell HTTP server with JSON state
- Vanilla JS SPA, no heavy framework
- Integrates with the Claude Agent SDK for AI features
- Optional Python worker for Gmail ingestion
- Read-only by design — cannot move money or initiate transactions

---

## Security model

- Local-only by default (binds to `localhost`)
- Session cookies: `HttpOnly`, `SameSite=Lax`, HMAC-signed, 7-day TTL
- Passwords: PBKDF2-SHA256, 100,000 iterations, per-user salt
- **Read-only integrations only.** Cairn observes and advises — it cannot
  move money, initiate transfers, or execute trades on your behalf
- When exposed remotely via a tunnel, your password is the only wall —
  choose a strong one

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

Copyright (c) 2026 Rook Atlas / Wesley Carpenter. All rights reserved.
See [LICENSE](LICENSE).

Cairn is proprietary software. Source is not publicly available during
private beta. An open-core release model is being evaluated for public
release.

---

## Contact

**Questions, beta access, partnership inquiries:**
w.carpenter226@gmail.com

Follow this repository for release announcements.
