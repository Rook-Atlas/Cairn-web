# Cairn

**Your money, marked out.**

Cairn is a self-hosted, privacy-first personal finance platform for households. A built-in AI companion called Ledger helps you understand where you stand and what to do next.

> **Status:** In development. Private beta. Public release planned Q3 2026.

## The problem

Every existing personal finance app asks you to do one of three things.

1. **Hand your bank credentials to a third party** that ultimately routes through services you don't control.
2. **Pay a monthly subscription** for a product you never actually own. If they shut down, get acquired, or change pricing, your budget history goes with them.
3. **Sell you something.** Investment products, credit cards, loans, advertising, or your aggregated behavior data.

Cairn rejects all three.

## The Cairn model

- **You own the data.** Everything lives as JSON on your machine.
- **You own the runtime.** Host Cairn on your own hardware.
- **AI where it actually helps.** Ledger, the built-in companion, answers questions grounded in your own data. No per-query API fees if you already have a Claude subscription.
- **Optional live bank sync.** Connect an aggregator for real-time transactions, or stay fully offline with CSV imports.
- **Built for households.** Multiple accounts, shared goals, shared timelines, with privacy controls between members.
- **Honest by design.** No false "safe to spend" numbers, no upsell funnels, no engagement hacks.

## What Cairn does

- **Traffic-light status.** Stable, tight, or short at a glance.
- **45-day payment timeline.** Every upcoming debit and credit, sorted by date and urgency, with running cash delta.
- **Past-due catch-up tracker.** One-time dig-out amounts ranked by real consequence (disconnects, credit reporting, late fees).
- **Levers view.** Income opportunities you haven't pulled yet (tax withholding, HRA reimbursements, loan optimization).
- **Lumpy-expense planner.** Sinking funds for inspections, vet bills, quarterly surprises.
- **CSV import** for Discover, Capital One, Chase, Ally, Best Buy Citi, and most US banks.
- **Gmail receipt parsing** (opt-in OAuth) for automatic bill ingestion.
- **Subscription detection** from your real transaction stream.

## Who it's for

- Privacy-minded people who don't want their transaction data flowing into third-party analytics pipelines.
- Households that need shared budgeting without exposing every detail.
- Developers and technically inclined users comfortable running a local service.
- Anyone burned by a finance app that shut down, got acquired, or changed pricing.

## Under the hood

- Self-hosted Windows service (Linux/Mac support planned)
- PowerShell HTTP server with JSON state
- Vanilla JS SPA, no heavy framework
- Integrates with the Claude Agent SDK for AI features
- Optional Python worker for Gmail ingestion
- Read-only by design. Cannot move money or initiate transactions.

## Security model

- Local-only by default. Binds to `localhost`.
- Session cookies are `HttpOnly`, `SameSite=Lax`, HMAC-signed, with a 7-day TTL.
- Passwords use PBKDF2-SHA256 at 100,000 iterations with per-user salt.
- **Read-only integrations only.** Cairn cannot move money, initiate transfers, or execute trades on your behalf.
- When exposed remotely via a tunnel, your password is the only wall. Choose a strong one.

## Planned integrations

- [x] CSV import (Discover, Capital One, Chase, Ally, Best Buy Citi)
- [x] Gmail receipt ingestion
- [ ] Plaid (transaction sync and balances). In review.
- [ ] Teller.io aggregator
- [ ] SimpleFIN Bridge
- [ ] Native email-alert parsing (no aggregator required)

## License

Copyright (c) 2026 Wesley Carpenter (d/b/a Rook Atlas). All rights reserved. See [LICENSE](LICENSE).

Cairn is proprietary software. Source is not publicly available during private beta. An open-core release model is being evaluated for public release.

## Contact

Questions, beta access, or partnership inquiries:
[rook.atlas@outlook.com](mailto:rook.atlas@outlook.com)

Follow this repository for release announcements.
