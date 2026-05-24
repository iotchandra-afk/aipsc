# My AI Product Strategy

> A living strategy built across 6 sessions. Each module adds one component. By Module 6, this repo IS your strategy — version-controlled, board-ready, portable.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [ ] | `01-the-bet/` |
| **The Moat** | M2 | [ ] | `02-the-moat/` |
| **The Margin** | M3 | [ ] | `03-the-margin/` |
| **The Contract** | M4 | [ ] | `04-the-contract/` |
| **The Guardrails** | M5 | [ ] | `05-the-guardrails/` |
| **The Pitch** | M6 | [ ] | `06-the-pitch/` |

---

- ## The Bet (M1)

What we're building, for whom, why now.

* Product: Relationship Intelligence OS
* AI Value Archetype: Orchestrator, with Oracle as secondary
* Vulnerability Scores: Moat 4/5 · Data 4/5 · Platform 3/5
* Top Risk: Platform absorption by Salesforce, Microsoft, ServiceNow, or another workflow platform if the product is reduced to a generic AI assistant or dashboard.
* Confidence: M
* Prototype: * Prototype: [Relationship Intelligence OS prototype](https://relation-graph-os.lovable.app)
* Kill Criteria: Kill or narrow the bet if users cannot understand the 360-degree signal synthesis, evidence trail, human approval model, and business metric impact within the prototype.

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

Why this will not be easy to copy in six months.

* Product: Relationship Intelligence OS
* Data Flywheel Score: 12/20
* Strongest Loop: Domain Context — 4/5
* Weakest Loop: Preference — 2/5
* Primary Moat Thesis: The moat is not access to customer, service, marketing, operations, digital, risk, and relationship data. The moat is the proprietary signal created when humans approve, edit, reject, override, and measure AI recommendations inside real relationship workflows.
* Most Valuable Created Signal: Human approval / edit / reject behavior tied to measurable outcomes.
* Primary Encroachment Threat: Salesforce Agentforce / Einstein / Data Cloud shipping a native relationship-moment assistant inside CRM and Service Cloud.
* Portability Score: Partial
* Kill Switch Summary: The product is strategically portable only if model calls, prompts, retrieval, tools, recommendation logic, evidence logging, human approval, and evals are separated from any single AI provider or workflow platform.
* 90-Day Defense: Build the preference loop, instrument approval/edit/reject/override behavior, create a retirement-transition eval set, and integrate into Salesforce, ServiceNow, and Microsoft surfaces rather than forcing users into another destination.

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

* Gross Margin (current): N/A — prototype-stage product
* Gross Margin (AI-adjusted): 83.4% estimated
* Pricing Model: Hybrid — enterprise platform fee + active-user fee + approved next-best-action allowance + overage
* Cascading Strategy: 80% non-frontier path / 20% frontier path
* Break-even at: $39.75 per active user / month before platform fee
→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

Why users will trust a probabilistic system.

* Reliability Target: Evidence fidelity ≥99%, approval-path correctness ≥99%, unsafe advice rate 0%, recommendation quality ≥4.2/5 on golden dataset.
* Golden Dataset: 15 starter rows, 8 adversarial; target is 100 rows before production pilot.
* Confidence UX: Tiered confidence with evidence strength, source freshness, missing-evidence warnings, and hard stops for unsafe or unevidenced recommendations.
* HITL Architecture: Five levels from no-review internal summaries to hard-stop blocks for hallucinated evidence, unauthorized advice, or policy conflict.
* Failure Mode Coverage: Hallucinated evidence, over-inference, unsafe tax/legal/suitability language, stale data, wrong role routing, evidence conflict, drift, and review overload.

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

What breaks when this scales — and what compounds.

* Compounding System: Observed signals → recommendation → evidence review → human decision → outcome movement → governed learning.
* Governance Posture: High-control pilot with evidence fidelity, unsafe-advice, approval, override, shadow-AI, and data-boundary gates before scale.
* Shadow AI Status: 12 tools / behaviors found; 8 governed or approved after triage; 4 killed.
* Agent Boundaries: Bounded agents only; observation, inference, recommendation, risk review, approval, routing, and outcome measurement must remain separated.
* Regulatory Exposure: High for financial-services deployment; Reg BI, FINRA supervision/communications, privacy, model risk, and EU AI Act screening must be handled before production scale.

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

How you get this funded, shipped, and adopted.

* Horizon 1 (Now): Publish the prototype and strategy repo, lock the retirement-transition wedge, define recommendation anatomy, event schema, golden dataset, AI gateway design, and governance owners.
* Horizon 2 (Next): Run a 90-day controlled validation pilot for retirement-transition next-best actions, preference memory, evidence fidelity, AI margin, and workflow integration.
* Horizon 3 (Bet): Expand only after wedge proof into beneficiary / estate journeys, campaign-to-service trend intelligence, advisor meeting prep, cross-business journey intelligence, and outcome-indexed pricing.
* Board Narrative: Relationship Intelligence OS turns fragmented financial-services relationship signals into governed, evidence-backed next-best actions that reduce service friction, improve advisor readiness, and create a compounding workflow moat.
* Key Metric: Cost per approved next-best action that moves a measurable business outcome.

→ Details: [`06-the-pitch/`](06-the-pitch/)
