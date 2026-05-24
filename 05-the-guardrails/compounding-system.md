# Compounding System Design

## Product

Product: Relationship Intelligence OS

Relationship Intelligence OS turns fragmented customer, service, sales/advice, marketing, digital, workplace, operations, document, and risk signals into governed, evidence-backed next-best actions for financial-services relationship work.

Primary AI Value Archetype: Orchestrator  
Secondary AI Value Archetype: Oracle

Prototype: https://relation-graph-os.lovable.app

---

## Module 5 Thesis

The product should not scale by adding more AI features. It should scale by making every approved recommendation, edit, rejection, override, and measured outcome improve the next decision.

The guardrail design must do two things at the same time:

1. Protect customers, advisors, associates, and the enterprise from unsafe AI behavior.
2. Turn governed usage into compounding product advantage.

The system should compound only from trusted work:

**Observed signals → recommendation → evidence review → human decision → outcome movement → governed learning**

Anything outside that chain is shadow AI risk, not product learning.

---

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|---|---|---|---|---|
| Recommendation Correction Loop | Approve, edit, request changes, decline, override reason | Better recommendation ranking, safer action bundles, improved prompts and retrieval | Y | Active in prototype design; not production-instrumented |
| Preference Memory Loop | Role, team, workflow, and risk-threshold behavior | Role-specific recommendation defaults and approval paths | Y | Missing; highest-priority build gap |
| Evidence Quality Loop | Evidence opened, missing evidence, stale evidence, source conflicts | Better evidence retrieval and stricter source requirements | Y | Partially designed |
| Outcome Learning Loop | Repeat contact, document rework, advisor readiness, planning coverage, approval rate, override rate | Outcome-weighted recommendation policies | Y | Designed; not yet proven |
| Risk Escalation Loop | Risk flags, policy conflicts, unsafe advice language, sensitive customer situations | Better escalation routing and hard-stop logic | Y | Partially designed |
| Shadow AI Loop | Unapproved tools, unsanctioned prompts, unmanaged workflows | Govern / kill / migrate decisions | Y, if captured | Missing |
| Enterprise Trend Loop | Campaign-to-service impact, journey friction, document defects, backlog pressure | Better planning, capacity, and journey design | Y | Partially designed |

### Broken loop identified by partner

Broken loop: **Preference Memory Loop**

The prototype shows role lenses, but it does not yet prove persistent role, team, workflow, or risk-threshold memory. A platform competitor could attack this by learning preferences directly inside CRM, ServiceNow, Microsoft Teams, Outlook, or advisor workflow surfaces.

### Fix plan

Build a governed preference memory layer with four levels:

1. **Role preference** — what each role needs from a recommendation
2. **Team preference** — how each team approves, edits, routes, or rejects actions
3. **Workflow preference** — how each journey type should be handled
4. **Risk preference** — which actions require stricter review

Every approval, edit, rejection, escalation, routing decision, and override reason should update the relevant preference profile only after governance rules allow reuse.

---

## Context Connectivity

The product’s compounding advantage depends on context connectivity. It must connect signals across channels and systems without collapsing customer privacy, data boundaries, or workflow control.

### Required context sources

| Context Source | Why It Matters | Guardrail |
|---|---|---|
| Customer / household profile | Establishes relationship context and eligibility | Access controlled by role and purpose |
| Service cases | Shows open work, repeat contact, friction, and unresolved issues | No customer-visible action without approval |
| Digital and mobile behavior | Surfaces early intent and journey signals | Use as signal, not proof of intent |
| Virtual assistant searches | Shows questions before a case is created | Do not infer intent from one search alone |
| Secure messages | Shows explicit customer language | Sensitive content requires stricter handling |
| Advisor / RM activity | Shows meeting readiness and relationship ownership | Respect business-unit and role boundaries |
| Workplace activity | Shows retirement and benefits journey signals | Use only within permitted purpose |
| Marketing engagement | Shows campaign-to-service interaction | Do not treat campaign click as customer instruction |
| Document operations | Shows defects, missing fields, rework drivers | Evidence must include source and timestamp |
| Risk / compliance controls | Defines escalation and hard stops | Controls must be workflow gates, not UI copy |
| Outcome metrics | Shows whether the recommendation changed the work | Must be tied to recommendation ID |

### Connectivity principle

The product should never say, “The AI knows this customer.”

It should say:

**“Here are the signals we observed, the inference we made, the action we recommend, the evidence supporting it, the risk boundary, and the approval required.”**

---

## Governance Policy

### Scope

Relationship Intelligence OS may support:

- Relationship-moment detection
- Retirement-transition preparation
- Service-work prioritization
- Document-defect remediation
- Advisor meeting preparation
- Campaign-to-service impact analysis
- Role-specific next-best-action recommendations
- Evidence-backed workflow routing
- Human-approved customer-facing draft preparation
- Outcome tracking after approved action

Relationship Intelligence OS may not autonomously:

- Provide tax advice
- Provide legal advice
- Make suitability determinations
- Recommend a securities transaction
- Recommend a specific investment product or allocation
- Execute money movement
- Change account data
- Send customer-visible communication without human approval
- Suppress risk flags
- Override policy controls
- Learn from sensitive customer data without approved governance

### Autonomy boundaries

| Autonomy Level | Allowed? | Example | Guardrail |
|---|---|---|---|
| Level 0: Observe | Yes | Detect omnichannel signals | Source and timestamp required |
| Level 1: Summarize | Yes | Summarize relationship context | Evidence trace required |
| Level 2: Recommend | Yes, with controls | Prepare retirement transition package | Human approval required |
| Level 3: Draft | Yes, with stricter controls | Draft service response | Human review required before use |
| Level 4: Route | Yes, with workflow policy | Send action to advisor queue | Routing logged and reversible |
| Level 5: Execute customer-visible action | No, not in current scope | Send outreach directly to customer | Hard stop |
| Level 6: Execute regulated financial action | No | Recommend trade, rollover decision, product allocation, money movement | Prohibited |

### Escalation triggers

Escalate to human review when:

- Action is customer-visible
- Customer sentiment indicates frustration or complaint risk
- Evidence is missing, stale, or conflicting
- Recommendation touches tax, legal, suitability, retirement income, estate, or investment implications
- Trusted contact or beneficiary issues are involved
- Fraud, account access, cash transfer, or unusual activity appears
- Business-unit policy conflict exists
- Confidence is below the approved threshold
- Model output includes advice-like language
- Recommendation requires judgment beyond operational preparation

### Audit cadence

| Audit Type | Cadence | Owner | Output |
|---|---|---|---|
| Recommendation quality review | Weekly during pilot | Product + Risk | Quality score and failure modes |
| Evidence fidelity audit | Weekly | Product + Data Governance | Source accuracy and missing evidence rate |
| Override reason review | Weekly | Product + Operations | Pattern analysis and product fixes |
| Shadow AI audit | Monthly | AI Governance + Technology Risk | Govern / migrate / kill list |
| Regulatory boundary review | Monthly during pilot | Legal / Compliance / Risk | Boundary updates and policy changes |
| Model / prompt change review | Every release | Product + Engineering + Risk | Eval report and release decision |
| Outcome review | Monthly | Business Owner + Product | Impact on repeat contact, rework, effort, advisor readiness |
| Executive governance review | Quarterly | Steering committee | Scale / hold / narrow decision |

### Regulatory exposure

This is a financial-services AI product. It should be treated as **high governance exposure** even if it is not automatically classified as high-risk under every jurisdiction.

| Regulatory / Policy Area | Exposure | Product Posture |
|---|---|---|
| SEC Reg BI / retail recommendation boundaries | High if product creates or implies securities recommendations | Do not recommend trades, securities, allocations, or rollover decisions. Keep product at preparation, evidence, workflow, and human-approved action level. |
| FINRA supervision / communications / books and records | High for broker-dealer environments | Treat AI usage as supervised technology. Log prompts, evidence, approvals, overrides, and customer-facing drafts. |
| Privacy and customer data protection | High | Use role-based access, data minimization, masking, audit trails, and purpose limitation. |
| EU AI Act | Medium screen; higher if creditworthiness, credit scoring, insurance risk, or essential-service eligibility is involved | Maintain AI inventory, risk classification, human oversight, technical documentation, and auditability. |
| Model risk management | Medium to high | Maintain evals, validation, drift monitoring, and change controls. |
| Marketing / communications compliance | Medium to high | Do not generate unapproved customer communication. Route drafts through approved review. |
| Operational risk | High | Track failure modes, review burden, outages, fallbacks, and escalation paths. |

### Governance posture

Governance posture: **High-control pilot**

The product should move forward only as a controlled pilot until the following are proven:

1. Evidence fidelity at or above 99%
2. Unsafe advice rate at 0%
3. Human approval compliance at 100% for customer-visible action
4. Override reasons captured and categorized
5. Recommendation outcomes measurable
6. Shadow AI tools inventoried and triaged
7. AI gateway and eval suite implemented
8. Production data boundaries approved

---

## Agent Topology

Relationship Intelligence OS should not be built as one general-purpose autonomous agent. It should use bounded agents with clear responsibilities, shared schemas, and strict escalation rules.

### Proposed agent topology

| Agent / Service | Purpose | Autonomy Level | Inputs | Outputs | Guardrail |
|---|---|---:|---|---|---|
| Signal Ingestion Service | Normalize signals across channels | 0 | Events, cases, messages, engagement, documents | Structured signal records | No inference beyond tagging |
| Evidence Retrieval Agent | Retrieve supporting evidence | 1 | Query, customer context, signal IDs | Evidence packet with source and timestamp | No recommendation without source |
| Relationship Moment Classifier | Detect journey type | 2 | Signal packet | Journey label and confidence | Must show uncertainty |
| Recommendation Composer | Build action bundle | 2 | Evidence, journey, role, policy | Draft next-best-action bundle | Human approval required |
| Risk Boundary Checker | Detect unsafe language and escalation needs | 2 | Recommendation draft, policy rules | Risk flags and approval path | Can block action |
| Role Lens Adapter | Reframe recommendation by role | 1 | Approved recommendation and role | Role-specific view | Cannot change underlying evidence |
| Customer-Facing Draft Assistant | Draft language after approval path is selected | 3 | Approved action, templates, policy | Draft response | Human review required |
| Workflow Router | Send approved work to proper queue | 4 | Approved action and role owner | Queue item / task | Logged and reversible |
| Outcome Measurement Service | Track metric movement | 1 | Recommendation ID, outcome data | Outcome report | No model-generated attribution without evidence |
| Governance Monitor | Watch evals, drift, overrides, usage, and risk events | 1 | Logs and telemetry | Alerts and governance reports | Escalates to humans |

### Agent design principle

No agent should have full authority to observe, infer, recommend, approve, communicate, and execute.

The system must separate:

- Observation
- Inference
- Recommendation
- Risk review
- Approval
- Execution
- Outcome measurement

This separation is the core guardrail.

---

## Shadow AI Audit

Shadow AI is the uncontrolled version of the same need. If users do not get governed relationship intelligence, they will use personal tools, browser extensions, meeting bots, spreadsheet macros, CRM notes, or unmanaged copilots to solve the work.

### Shadow AI inventory

| Tool / Behavior | Owner | Risk Level | Decision |
|---|---|---:|---|
| Personal ChatGPT / Claude prompts using copied customer context | Individual associates / RMs | H | Kill for customer data; provide approved internal alternative |
| Unapproved meeting transcript tools | Advisor / RM teams | H | Govern or kill depending on data handling and consent |
| Spreadsheet-based “next-best-action” scoring | Operations analysts | M | Govern and migrate logic into approved workflow |
| CRM notes summarized through browser extensions | Sales / service users | H | Kill if customer data leaves approved environment |
| Personal prompt libraries for customer emails | Relationship teams | H | Govern through approved templates and review |
| Marketing campaign analysis using external AI tools | Marketing analysts | M | Govern; restrict customer-level data; allow aggregate analysis only |
| Service-case clustering in unmanaged notebooks | Analytics teams | M | Govern; migrate into approved environment |
| AI-generated customer-facing language outside approved review | Associates / advisor teams | H | Kill; route through approved draft and supervision workflow |
| Internal productivity copilot for non-customer notes | Knowledge workers | L | Keep with policy and data controls |
| Vendor AI features embedded in CRM / workflow platforms | Platform teams | M | Govern through AI inventory, evals, data agreements, and controls |
| Local summarization of public product / policy content | Product / training teams | L | Keep with citation and review controls |
| Manual copy-paste between systems to create briefings | Associates / RMs | M | Migrate into Relationship Intelligence OS workflow |

### Shadow AI triage summary

Total tools / behaviors found: **12**

| Decision | Count |
|---|---:|
| Keep | 2 |
| Govern | 6 |
| Kill | 4 |

Tools after triage: **8 governed or approved patterns**

Estimated hidden spend: **Unknown at prototype stage**

Estimated hidden risk: **High**, because the highest-risk behaviors involve customer data, customer-facing language, and unmanaged AI tools outside the approved control environment.

### Shadow AI operating rule

Do not merely ban shadow AI. Replace the underlying job-to-be-done with a governed product surface.

If users copy customer context into unmanaged tools, the need is real. The product must offer:

- Evidence-backed relationship brief
- Approved prompt templates
- Human approval
- Source traceability
- Customer data controls
- Customer-facing language review
- Audit logging
- Outcome tracking

---

## Compounding System Architecture

The compounding system should turn safe usage into product advantage.

### Learning layers

| Layer | What It Learns | Reuse Boundary |
|---|---|---|
| Customer-level memory | Customer-specific signals, open work, prior recommendations, approvals | Private to authorized users for that customer / household |
| Role-level memory | What each role needs from the recommendation | Reusable across role under governance |
| Team-level memory | Approval, edit, reject, routing, and escalation patterns | Reusable within team |
| Workflow-level memory | Journey-specific patterns such as retirement transition, rollover, beneficiary, document defect | Reusable across approved workflows |
| Business-unit memory | Segment and operating-model patterns | Reusable within business unit |
| Enterprise pattern memory | Anonymized journey intelligence | Reusable only after governance approval |

### Learning events

Capture these as structured events:

- Recommendation shown
- Evidence opened
- Evidence missing
- Evidence conflict found
- Action approved
- Action edited
- Action declined
- Override reason submitted
- Action routed
- Supervisor review triggered
- Risk review triggered
- Customer-facing draft approved
- Outcome metric observed
- Recommendation later judged inaccurate
- Customer complaint or friction event linked to recommendation

### Learning rules

The system should learn only when:

1. The event is logged.
2. The evidence is traceable.
3. The human decision is known.
4. The outcome is measurable or explicitly unknown.
5. The data boundary permits reuse.
6. The use case has passed eval and policy review.

The system should not learn from:

- Unapproved customer data
- Unmanaged user prompts
- Hallucinated evidence
- Unsafe recommendations
- Customer complaints without review
- Data outside permitted purpose
- Free-text overrides without taxonomy
- Shadow AI outputs

---

## Guardrail Taxonomy

| Guardrail Type | Purpose | Example |
|---|---|---|
| Data guardrail | Prevent misuse of customer-sensitive data | Role-based access, masking, purpose limitation |
| Evidence guardrail | Prevent hallucinated or unsupported recommendations | Source, timestamp, lineage required |
| Action guardrail | Prevent unsafe customer impact | Human approval before outreach |
| Advice-boundary guardrail | Prevent tax, legal, suitability, or investment recommendation overreach | Block advice-like language |
| Workflow guardrail | Keep actions inside approved operating paths | Route to RM, service, risk, or advisor queue |
| Evaluation guardrail | Prevent model or prompt changes from degrading quality | Golden dataset release gate |
| Governance guardrail | Create accountability and auditability | Approval logs, override taxonomy, review cadence |
| Cost guardrail | Prevent margin erosion from uncontrolled AI usage | AI gateway, model routing, usage thresholds |
| Vendor guardrail | Prevent platform lock-in | Provider abstraction and eval-driven routing |
| Shadow AI guardrail | Prevent unmanaged tools from bypassing controls | Inventory, triage, migrate, kill |

---

## Abuse and Failure Scenarios

| Scenario | Risk | Guardrail |
|---|---|---|
| Associate copies customer profile into external chatbot | Customer data exposure | Kill behavior; provide approved internal briefing workflow |
| AI infers retirement transition from one article click | Over-inference | Confidence threshold and signal sufficiency rule |
| AI drafts tax guidance for rollover | Regulatory and customer harm | Hard stop; route to human review; educational-only framing |
| Advisor receives briefing with stale data | Bad customer experience | Source freshness warning and stale-evidence block |
| Marketing uses individual-level intent without permission | Privacy / consent risk | Purpose limitation and aggregate-only analysis |
| Risk reviewer cannot see evidence chain | Audit failure | Evidence lineage required before approval |
| Recommendation creates more review burden than value | Operating failure | Track human review burden and cost per approved action |
| Model vendor changes output style | Reliability drift | Eval gate before release |
| User approves without opening evidence | Rubber-stamp risk | Evidence-prompt requirement for medium/high-risk items |
| Agent routes work to wrong queue | Workflow harm | Reversible routing and audit log |

---

## Scale Readiness Checklist

Relationship Intelligence OS should not scale beyond controlled pilot unless these are true:

1. AI inventory exists for all model-enabled workflows.
2. Golden dataset has at least 100 labeled examples.
3. Evidence fidelity is at or above 99%.
4. Unsafe advice rate is 0%.
5. Human approval compliance is 100% for customer-visible action.
6. AI gateway exists.
7. Provider abstraction exists.
8. Prompts are versioned.
9. Recommendation schema is enforced.
10. Evidence lineage is logged.
11. Override reasons are categorized.
12. Outcome metrics are tied to recommendation IDs.
13. Role and team preferences are captured as structured events.
14. Shadow AI inventory is complete.
15. Shadow AI triage has keep / govern / kill decisions.
16. Risk, legal, compliance, product, engineering, and business owners have named accountability.
17. Drift monitoring exists.
18. Cost telemetry exists.
19. Incident response path exists.
20. Production data-boundary approval exists.

---

## 30-Day Guardrail Build Plan

### Week 1: Establish AI inventory and governance spine

- Inventory current AI use cases and shadow AI patterns.
- Classify each as keep / govern / kill.
- Define approved and prohibited customer-data uses.
- Confirm scope of Relationship Intelligence OS pilot.
- Define autonomy levels.
- Name product, risk, compliance, engineering, and business owners.

### Week 2: Build control architecture

- Define AI gateway requirements.
- Define recommendation schema.
- Define evidence schema.
- Define approval-event schema.
- Define override-reason taxonomy.
- Define risk escalation triggers.
- Define customer-facing communication controls.

### Week 3: Instrument compounding loops

- Capture approve / edit / reject / override behavior.
- Capture evidence-open behavior.
- Capture action-bundle changes.
- Capture role-lens use.
- Capture routing changes.
- Capture outcome metrics.
- Capture review burden.

### Week 4: Run governance simulation

Run four simulations:

1. AI recommends unsafe rollover language.
2. Evidence is missing for beneficiary status.
3. User attempts to export customer context into unmanaged tool.
4. Salesforce ships a native relationship-moment assistant.

For each simulation, document:

- Detection path
- Product response
- Human owner
- Audit record
- Customer impact
- Business decision
- Required product change

---

## Final Assessment

Relationship Intelligence OS should scale only as a governed compounding system.

The product’s advantage is not that it uses AI. The advantage is that it captures the judgment of relationship managers, service associates, advisors, marketers, operations leaders, and risk reviewers inside real workflows, then uses that governed signal to improve future actions.

The hard line:

**No evidence, no recommendation. No approval, no customer impact. No outcome, no moat.**
