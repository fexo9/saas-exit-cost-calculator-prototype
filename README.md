# SaaS Exit Cost Calculator — PROTOTYPE

**This is a discovery prototype, not a product. Not for sale. No buy link, no price, no offer.**

It answers one question: *what does your subscription really cost once price hikes compound — and what does a one-time alternative cost over the same years, fairly counted?*

## What it does

Enter your monthly fee, expected annual price-hike %, years, seats, and the one-time alternative's price. The calculator shows:

- Per-year subscription cost with compounding hikes
- Cumulative subscription total
- One-time route total: purchase + migration/setup + annual upkeep (hosting, maintenance, updates)
- The difference — in either direction

## Why the comparison is fair

An earlier version only counted the one-time purchase price. That was biased: it ignored what switching and keeping a one-time tool actually costs. This version (v1.1) adds:

- **Migration / setup cost** on the one-time side (optional, defaults to 0)
- **Annual upkeep** on the one-time side (optional, defaults to 0)
- **Annual-billing discount** on the subscription side (optional, defaults to 0)

If the one-time route's migration + upkeep exceed the savings, the calculator says the subscription wins. That is the honest answer, and it is shown, not hidden.

## What it does NOT model

Switching effort (data export, retraining, downtime), the risk that a one-time tool is abandoned or stops updating, and anything the subscription buys beyond access (support, integrations, compliance). Estimate those separately before deciding anything.

## Status

Prototype for a discovery experiment. It is not a commercial product. It will only become one if real buyer evidence ever justifies it — and only after the usual validation gates.

## Run it

Open `saas-exit-cost-calculator-prototype.html` in any browser. No build step, no server, no data leaves your machine.

## Tests

`test-saas-exit-cost-calculator.js` — 23 deterministic checks (run with `node`). All pass, including the fairness cases: defaults reproduce the v1.0 numbers, migration + upkeep reduce savings, the annual discount reduces the subscription total, and an expensive migration makes the one-time route honestly lose.
