# Relationship Intelligence OS — AI Product Strategy

> A living AI product strategy built across six modules. This repo defines the bet, moat, margin, trust contract, guardrails, and board pitch for Relationship Intelligence OS.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|---|---|---|---|
| The Bet | M1 | Complete | `01-the-bet/` |
| The Moat | M2 | Complete | `02-the-moat/` |
| The Margin | M3 | Complete | `03-the-margin/` |
| The Contract | M4 | Complete | `04-the-contract/` |
| The Guardrails | M5 | Complete | `05-the-guardrails/` |
| The Pitch | M6 | Complete | `06-the-pitch/` |

---

## Product

**Relationship Intelligence OS**

Relationship Intelligence OS is an AI-native enterprise product for large financial-services firms. It turns fragmented customer, service, sales/advice, marketing, digital, workplace, operations, document, and risk signals into governed, evidence-backed next-best actions.

This is not a chatbot.  
This is not a generic dashboard.  
This is not a thin CRM copilot.  

It is an operating intelligence layer for relationship work.

**Prototype:** [Relationship Intelligence OS prototype](https://relation-graph-os.lovable.app)

---

## The Bet (M1)

What we are building, for whom, and why now.

* Product: Relationship Intelligence OS
* AI Value Archetype: Orchestrator, with Oracle as secondary
* Vulnerability Scores: Moat 4/5 · Data 4/5 · Platform 3/5
* Top Risk: Platform absorption by Salesforce, Microsoft, ServiceNow, or another workflow platform if the product is reduced to a generic AI assistant or dashboard.
* Confidence: Medium
* Prototype: [Relationship Intelligence OS prototype](https://relation-graph-os.lovable.app)
* Kill Criteria: Kill or narrow the bet if users cannot understand the 360-degree signal synthesis, evidence trail, human approval model, and business metric impact within the prototype.

→ Details: `01-the-bet/`

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

→ Details: `02-the-moat/`

---

## The Margin (M3)

Will this make money or bleed it?

* Gross Margin (current): N/A — prototype-stage product
* Gross Margin (AI-adjusted): 83.4% estimated
* Pricing Model: Hybrid — enterprise platform fee + active-user fee + approved next-best-action allowance + overage
* Cascading Strategy: 80% non-frontier path / 20% frontier path
* Break-even at: $39.75 per active user / month before platform fee
* Key Economic Unit: Cost per approved next-best action that moves a measurable business outcome.

→ Details: `03-the-margin/`

---

## The Contract (M4)

Why users will trust a probabilistic system.

* Reliability Target: Evidence fidelity ≥99%, approval-path correctness ≥99%, unsafe advice rate 0%, recommendation quality ≥4.2/5 on golden dataset.
* Golden Dataset: 15 starter rows, 8 adversarial; target is 100 rows before production pilot.
* Confidence UX: Tiered confidence with evidence strength, source freshness, missing-evidence warnings, and hard stops for unsafe or unevidenced recommendations.
* HITL Architecture: Five levels from no-review internal summaries to hard-stop blocks for hallucinated evidence, unauthorized advice, or policy conflict.
* Failure Mode Coverage: Hallucinated evidence, over-inference, unsafe tax/legal/suitability language, stale data, wrong role routing, evidence conflict, drift, and review overload.

→ Details: `04-the-contract/`

---

## The Guardrails (M5)

What breaks when this scales — and what compounds.

* Compounding System: Observed signals → recommendation → evidence review → human decision → outcome movement → governed learning.
* Governance Posture: High-control pilot with evidence fidelity, unsafe-advice, approval, override, shadow-AI, and data-boundary gates before scale.
* Shadow AI Status: 12 tools / behaviors found; 8 governed or approved after triage; 4 killed.
* Agent Boundaries: Bounded agents only; observation, inference, recommendation, risk review, approval, routing, and outcome measurement must remain separated.
* Regulatory Exposure: High for financial-services deployment; Reg BI, FINRA supervision/communications, privacy, model risk, and EU AI Act screening must be handled before production scale.

→ Details: `05-the-guardrails/`

---

## The Pitch (M6)

How this gets funded, shipped, and adopted.

* Horizon 1 (Now): Publish the prototype and strategy repo, lock the retirement-transition wedge, define recommendation anatomy, event schema, golden dataset, AI gateway design, and governance owners.
* Horizon 2 (Next): Run a 90-day controlled validation pilot for retirement-transition next-best actions, preference memory, evidence fidelity, AI margin, and workflow integration.
* Horizon 3 (Bet): Expand only after wedge proof into beneficiary / estate journeys, campaign-to-service trend intelligence, advisor meeting prep, cross-business journey intelligence, and outcome-indexed pricing.
* Board Narrative: Relationship Intelligence OS turns fragmented financial-services relationship signals into governed, evidence-backed next-best actions that reduce service friction, improve advisor readiness, and create a compounding workflow moat.
* Key Metric: Cost per approved next-best action that moves a measurable business outcome.

→ Details: `06-the-pitch/`

---

## Final Board Narrative

Relationship Intelligence OS should be funded as a controlled AI product bet, not as a broad transformation program.

The product starts with one disciplined wedge:

**Retirement transition → governed next-best action → measurable workflow improvement → compounding preference memory.**

The strategic bet is narrow enough to validate, important enough to matter, and hard enough to prove whether the enterprise can build AI products that are reliable, economical, governed, and defensible.

---

## Final Assessment

Relationship Intelligence OS is strategically credible if it stays focused on workflow-specific signal, governed action, and outcome-linked learning.

The product should not compete on model access.  
It should not compete as a chatbot.  
It should not compete as another dashboard.  

It should compete as the trusted action layer for financial-services relationship work.

Hard line:

**No evidence, no recommendation. No approval, no customer impact. No outcome, no moat.**
