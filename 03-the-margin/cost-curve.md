# Cost Curve & Pricing Strategy

## Product

Product: Relationship Intelligence OS

Relationship Intelligence OS is an AI-native enterprise product for large financial-services firms. It turns fragmented customer, service, sales/advice, marketing, digital, workplace, operations, document, and risk signals into governed, evidence-backed next-best actions.

Primary AI Value Archetype: Orchestrator  
Secondary AI Value Archetype: Oracle

Prototype: https://relation-graph-os.lovable.app

---

## Margin Thesis

Relationship Intelligence OS should not be priced like a simple SaaS seat. The product creates value by changing work: earlier relationship intervention, fewer repeat contacts, lower document rework, better advisor preparation, and more governed next-best actions.

The margin risk is that AI usage scales with every signal, recommendation, evidence panel, role lens, approval workflow, and evaluation run. If every workflow defaults to frontier-model reasoning, the product will look impressive in demos and weak in production economics.

The economic design must do three things:

1. Route simple work to cheaper paths.
2. Reserve frontier reasoning for high-value or high-risk decisions.
3. Price against the unit of value, not only the user seat.

The core economic unit should be:

**Approved next-best action**

A user seat creates access. An approved next-best action creates measurable business value.

---

## Cost Model

### Cost model assumptions

This is a prototype-stage estimate, not a production quote.

Assumptions:

- Customer type: large financial-services enterprise
- Primary user: service associate, relationship manager, advisor team member, marketing partner, operations leader, or risk reviewer
- Pricing unit: active user per month plus approved next-best-action volume
- Average active user workload: 120–180 relationship intelligence events per month
- Average approved next-best actions: 35 per active user per month
- Human approval remains required before customer-visible action
- Most signal triage, classification, retrieval, and formatting should not use a frontier model
- Frontier reasoning should be reserved for complex inference, risk-sensitive recommendations, and edge cases

### Estimated AI COGS per active user per month

| Cost Category | Per-User / Month | Notes |
|---|---:|---|
| Inference — triage / small model | $4.80 | Channel classification, signal tagging, simple summaries, evidence extraction, role-lens formatting |
| Inference — frontier model | $11.20 | Complex reasoning, ambiguous relationship moments, high-risk recommendations, multi-signal synthesis |
| Embeddings / retrieval | $2.50 | Search over customer signals, cases, policy references, marketing engagement, service history, and evidence records |
| Infrastructure / orchestration | $4.00 | AI gateway, workflow orchestration, queueing, latency controls, observability |
| Data / storage / logging | $2.25 | Evidence logs, recommendation lineage, approval records, audit events, outcome history |
| Human-in-the-loop quality review | $9.00 | Sampling, supervisor review, exception review, risk escalation, override analysis |
| Security / compliance / controls allocation | $6.00 | Permissioning, audit trail, monitoring, policy checks, data-boundary controls |
| **Total AI COGS** | **$39.75** | Estimated variable and semi-variable cost per active user per month |

### Gross margin view

| Metric | Estimate |
|---|---:|
| Proposed base price per active user / month | $240.00 |
| Estimated AI COGS per active user / month | $39.75 |
| Gross profit per active user / month | $200.25 |
| AI-adjusted gross margin | 83.4% |

### Interpretation

The product can support strong gross margin if the AI architecture is disciplined.

The risk is not the average user. The risk is the heavy user, the high-friction workflow, and the poorly routed model call path. A small number of power users could consume disproportionate inference, retrieval, and review capacity if pricing and routing are not controlled.

The economic design must avoid three failure modes:

1. Unlimited frontier reasoning under flat seat pricing.
2. Recommendation generation without outcome measurement.
3. Human review burden growing faster than work reduction.

---

## Cascading Strategy

Module 3’s core routing principle is model cascading: route simpler work to cheaper models and reserve frontier models for harder, higher-risk work. The course reference card frames 80/20 as a starting scaffold, not a rule. :contentReference[oaicite:2]{index=2}

### Routing design

| Tier | Share of Requests | What It Handles | Model / Method |
|---|---:|---|---|
| Deterministic / rules / cache | 12% | Known workflow rules, permission checks, policy gates, repeated evidence summaries, formatting | Rules, cache, retrieval, workflow logic |
| Small / cheaper model | 68% | Signal tagging, channel classification, low-risk summarization, role-lens formatting, simple evidence extraction | Low-cost model |
| Frontier model | 20% | Multi-signal inference, ambiguous relationship moments, risk-sensitive next-best actions, complex recommendation synthesis | Frontier model |

Expected cascade ratio:

**80% non-frontier path / 20% frontier path**

This includes deterministic, cached, retrieval-based, and small-model work in the non-frontier path.

### Task-level routing

| Workflow | Default Path | Escalate to Frontier When |
|---|---|---|
| Signal tagging | Small model | Conflicting signals or missing context |
| Channel classification | Rules / small model | Unclassified source or risk-sensitive signal |
| Evidence extraction | Retrieval / small model | Evidence conflicts or customer-visible action depends on interpretation |
| Relationship moment detection | Small model first | Multi-domain signal synthesis is required |
| Next-best-action generation | Frontier model for first version | Can later cascade once evals prove quality |
| Customer-facing draft | Frontier or approved mid-tier model | Any advice boundary, suitability, legal, tax, or risk issue appears |
| Role-lens formatting | Small model / template | Executive or risk-review version requires more precise framing |
| Trend pulse | Batch job / small model | Enterprise-wide anomaly requires deeper analysis |
| Trust and controls | Rules first | Ambiguous approval path or policy conflict |

### Margin controls

| Lever | Action |
|---|---|
| Caching | Cache stable relationship summaries, policy snippets, and repeated evidence chains |
| Prompt optimization | Reduce context size by sending structured evidence, not full raw history |
| Retrieval filtering | Retrieve only signals relevant to the journey type and user role |
| Frontier gating | Require business value or risk threshold before frontier call |
| Batch processing | Run trend intelligence in scheduled batches, not live per user |
| Eval-based routing | Move repeated safe workflows to cheaper models only after passing evals |
| Human review sampling | Sample by risk, uncertainty, and override rate, not flat percentage |

---

## Pricing Model

The course frames three pricing models: seat-based, hybrid, and outcome-based. Hybrid is the right posture for most AI products, while outcome-based works when the unit of work is cleanly measurable. :contentReference[oaicite:3]{index=3}

### Current pricing

Current pricing: **None — prototype-stage product**

The current product is not yet commercial. For the purpose of Module 3, the pricing strategy is modeled as an enterprise B2B product sold to large financial-services organizations.

### Proposed AI pricing

Pricing model: **Hybrid**

Structure:

1. Annual enterprise platform fee
2. Active-user monthly fee
3. Included monthly approved next-best-action allowance
4. Overage fee for approved next-best actions above allowance
5. Add-on pricing for high-cost workflows

### Proposed pricing structure

| Pricing Element | Proposed Price | Rationale |
|---|---:|---|
| Annual platform fee | $250,000 / year | Covers enterprise setup, security review, integrations, governance, reporting, and platform access |
| Active user fee | $240 / active user / month | Captures ongoing workflow value while protecting against inactive-seat inflation |
| Included next-best actions | 35 approved actions / active user / month | Aligns usage with normal relationship-work volume |
| Overage fee | $1.50 / approved action | Protects margin when usage scales beyond normal behavior |
| High-complexity workflow add-on | Custom | Applies to heavy agentic workflows, deep portfolio analysis, or highly regulated custom journeys |

### Unit of value

Primary unit of value:

**Approved next-best action**

Secondary units of value:

- Relationship moment detected
- Repeat contact avoided
- Document rework avoided
- Advisor meeting readiness improved
- Planning coverage improved
- Human-approved recommendation completed

### Why not pure seat pricing

Pure seat pricing is risky because AI cost is usage-sensitive. Two users may pay the same seat price while one runs ten times more recommendations, evidence expansions, and workflow actions.

Pure seat pricing would subsidize heavy users and punish light users. It would also hide whether the product is creating real value.

### Why not pure outcome pricing yet

Pure outcome pricing is not ready because attribution will be difficult early.

For example, if repeat contacts fall, the improvement may come from better recommendations, staffing changes, seasonality, workflow cleanup, policy changes, or marketing changes. Outcome pricing can come later, but the product first needs reliable instrumentation and customer trust.

### Final pricing posture

The right posture is:

**Hybrid pricing now; outcome-indexed expansion later.**

The enterprise buyer pays for platform readiness and active users. Heavy usage is governed through approved-action allowances and overage. As outcome measurement matures, pricing can evolve toward value-share or outcome-indexed contracts.

---

## Leader / Filler / Killer Packaging

The course’s Leader / Filler / Killer framework separates the core reason users buy from lightweight bundle features and heavy-cost features that may need separate pricing. It also uses the 70% rule: if more than 70% of users touch a feature, bundle it; if fewer, consider pricing it separately. :contentReference[oaicite:4]{index=4}

| Role | Feature in Relationship Intelligence OS | Packaging Decision |
|---|---|---|
| Leader | Governed next-best-action engine | Bundle into core product |
| Filler | Relationship summaries, role-lens views, signal timeline, evidence chips | Bundle into core product |
| Killer | Deep agentic workflow execution, complex multi-system remediation, high-volume autonomous research, custom journey modeling | Price as add-on or usage-based expansion |

### 70% rule interpretation

Expected usage:

- Relationship summaries: >70% of active users
- Evidence trail: >70% of active users
- Next-best-action review: >70% of active users
- Role-lens views: >70% of active users
- Deep agentic workflow execution: <30% of active users
- Custom enterprise trend modeling: <30% of active users

Decision:

Bundle the core intelligence and evidence workflow. Price heavy agentic execution separately.

---

## Stress Tests

### Scenario summary

| Scenario | Impact on Margin | Response |
|---|---|---|
| Inference costs 3x | AI COGS rises from $39.75 to approximately $71.75 per active user / month. Gross margin falls from 83.4% to approximately 70.1%. | Freeze non-critical frontier usage, increase cascading, cache more evidence chains, move repeated safe workflows to cheaper models after evals, preserve human approval and risk controls. |
| Heaviest segment doubles usage | Heavy users consume more recommendations, evidence expansions, and review capacity. Margin compresses if usage remains under flat seat pricing. | Enforce approved-action allowance, trigger overage pricing, throttle low-value workflows, route high-volume summaries to cheaper models, monitor cost per approved action. |
| Model provider raises prices 50% | AI COGS rises from $39.75 to approximately $47.75 per active user / month. Gross margin falls from 83.4% to approximately 80.1%. | Activate provider-cost review, reroute low-risk tasks, use cached outputs, evaluate provider alternatives, protect frontier reasoning for risk-sensitive recommendations. |
| Human review burden doubles | Total AI COGS rises materially because HITL review is one of the largest cost components. | Sample by risk and uncertainty, improve evidence quality, create approval templates, strengthen evals, reduce ambiguous recommendations. |
| Customer-facing draft volume spikes | Frontier usage and review burden rise together. | Require action-value threshold, reuse approved templates, cache safe language patterns, keep human approval required. |

### Stress Test 1: Inference costs 3x

Current estimated AI COGS:

**$39.75 per active user / month**

Estimated AI COGS under 3x inference costs:

**$71.75 per active user / month**

Gross margin impact at $240 active-user price:

| Metric | Current | Under 3x Inference |
|---|---:|---:|
| Revenue / active user / month | $240.00 | $240.00 |
| AI COGS / active user / month | $39.75 | $71.75 |
| Gross profit / active user / month | $200.25 | $168.25 |
| Gross margin | 83.4% | 70.1% |

Interpretation:

The product remains viable under a 3x inference shock, but the margin buffer narrows sharply. The response should not be across-the-board quality reduction. It should be routing discipline.

Response:

- Keep frontier reasoning for high-risk recommendations.
- Move low-risk summaries, classification, and role formatting to cheaper models.
- Expand caching for stable evidence chains.
- Use deterministic rules for policy and permission gates.
- Reduce unnecessary regeneration.
- Monitor cost per approved next-best action.
- Pause low-value experimentation.

### Stress Test 2: Heaviest segment doubles usage

Risk:

The highest-cost users are likely relationship managers, service leads, risk reviewers, and operations leaders handling complex journeys. If their usage doubles under flat seat pricing, they could consume disproportionate model, retrieval, and human review capacity.

Margin problem:

The product would still receive $240 per active user, but costs could rise from approximately $39.75 to $60–$75 per heavy user before overage or add-on pricing.

Response:

- Define normal usage allowance.
- Charge overage per approved next-best action.
- Separate “view intelligence” from “generate complex recommendation.”
- Track cost per workflow, not only cost per user.
- Price deep agentic workflows separately.
- Add admin controls for usage budgets and approval thresholds.

### Stress Test 3: Model provider raises prices 50%

Estimated impact:

| Metric | Current | 50% Provider Increase |
|---|---:|---:|
| AI COGS / active user / month | $39.75 | $47.75 |
| Gross margin | 83.4% | 80.1% |

Response:

- Activate provider-routing review.
- Keep high-risk workflows on approved quality path.
- Route low-risk work to cheaper models or deterministic methods.
- Run evals before switching any recommendation workflow.
- Communicate margin impact to business sponsors.
- Maintain human approval and evidence logging.

---

## Break-Even View

### Per-user break-even

Estimated AI COGS per active user:

**$39.75 per month**

Proposed active-user price:

**$240 per month**

Break-even active-user price before platform fee:

**$39.75 per month**

This means the active-user price has a 6.0x coverage ratio over estimated AI COGS.

### Enterprise account break-even

Illustrative customer:

- 1,000 active users
- $240 per active user / month
- $250,000 annual platform fee

Annual revenue:

| Revenue Component | Annual Revenue |
|---|---:|
| Platform fee | $250,000 |
| Active-user fees | $2,880,000 |
| Estimated total annual revenue | $3,130,000 |

Annual AI COGS:

| Cost Component | Annual Cost |
|---|---:|
| AI COGS per active user / month | $39.75 |
| Active users | 1,000 |
| Months | 12 |
| Estimated annual AI COGS | $477,000 |

Estimated annual gross profit:

**$2,653,000**

Estimated gross margin:

**84.8%**

Interpretation:

At enterprise scale, the product can support attractive gross margin if the average active user remains near the modeled cost curve. The platform fee helps absorb governance, security, and integration overhead. The overage model protects against heavy users.

---

## Board One-Pager

### Before: traditional SaaS / workflow platform economics

A traditional enterprise SaaS product charges for access. Gross margin is strong because marginal software usage is cheap. The economic risk is mostly implementation, support, and customer success.

Representative model:

| Metric | Traditional SaaS View |
|---|---:|
| Price / user / month | $160 |
| COGS / user / month | $24 |
| Gross margin | 85% |
| Pricing logic | Seat access |
| Risk | Adoption and renewal |

### After: AI-enabled operating intelligence economics

Relationship Intelligence OS charges for access plus governed work completed. Gross margin remains strong only if AI usage is routed, measured, and priced correctly.

Representative model:

| Metric | AI-Enabled View |
|---|---:|
| Price / active user / month | $240 |
| AI COGS / active user / month | $39.75 |
| Gross margin | 83.4% |
| Pricing logic | Hybrid: active user + approved next-best-action usage |
| Risk | Heavy users, frontier-model overuse, human review burden, provider price shock |

### Net margin shift

The AI-enabled product has slightly lower gross margin percentage than traditional SaaS, but materially higher revenue per active user and stronger value capture.

| Metric | Traditional SaaS | Relationship Intelligence OS |
|---|---:|---:|
| Revenue / user / month | $160 | $240 |
| COGS / user / month | $24 | $39.75 |
| Gross profit / user / month | $136 | $200.25 |
| Gross margin | 85.0% | 83.4% |

Net margin shift:

**Gross margin percentage declines by 1.6 points, but gross profit per active user increases by $64.25 per month.**

### Board-level conclusion

Relationship Intelligence OS should be funded only if the team manages AI economics as a product system, not as an infrastructure afterthought.

The product can make money if:

1. Frontier models are reserved for high-value reasoning.
2. Simple work is routed to cheaper paths.
3. Human approval is risk-based, not blanket-heavy.
4. Pricing includes active-user and usage-based protection.
5. The primary unit of value is approved next-best action.
6. The product measures outcomes, not AI activity.

The business should not chase usage for its own sake. It should optimize for:

**Cost per approved next-best action that moves a measurable business outcome.**

---

## Final Assessment

Relationship Intelligence OS has viable AI economics if it avoids flat unlimited usage and frontier-model defaulting.

The recommended pricing model is:

**Enterprise platform fee + active-user fee + included approved-action allowance + overage for heavy usage + add-ons for expensive agentic workflows.**

Current gross margin estimate:

**83.4% AI-adjusted gross margin**

Stress-tested gross margin under 3x inference costs:

**70.1%**

The product should proceed only with clear cost telemetry:

- Cost per active user
- Cost per recommendation shown
- Cost per approved next-best action
- Cost per outcome moved
- Frontier-model utilization
- Human review burden
- Override rate
- Recommendation acceptance rate
- Repeat-contact reduction
- Document-rework reduction
- Advisor-readiness improvement

The margin strategy is not “AI will get cheaper.”

The margin strategy is:

**Route intelligently. Price against value. Measure the work changed.**
