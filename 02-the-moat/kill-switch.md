# Kill Switch Audit

## Product

Product: Relationship Intelligence OS

Relationship Intelligence OS is an AI-native enterprise product for large financial-services firms. It turns fragmented customer, service, sales/advice, marketing, digital, workplace, operations, document, and risk signals into governed, evidence-backed next-best actions.

This is not a chatbot. It is not a generic dashboard. It is not a thin CRM copilot.

The product’s defensibility depends on whether it can own the workflow from signal detection to human-approved action to measured business outcome.

Primary AI Value Archetype: Orchestrator  
Secondary AI Value Archetype: Oracle

Prototype: https://relation-graph-os.lovable.app

---

## Primary Dependency Risk

The primary dependency risk is not the current Lovable prototype. Lovable is a prototype-generation and hosting dependency, not the long-term strategic risk.

The strategic dependency risk is that the future product becomes too dependent on one AI provider, one model family, one CRM/workflow platform, or one retrieval architecture.

If Relationship Intelligence OS hard-codes model calls, prompts, retrieval patterns, tool calls, evaluation logic, or workflow actions around a single provider, the product becomes strategically exposed. Pricing changes, degraded model quality, policy changes, latency issues, data-boundary concerns, or a competing vendor feature could damage the product quickly.

The product must avoid competing on model access. It should compete on:

- Cross-domain financial-services signal model
- Human approval / edit / reject history
- Role and team preference memory
- Evidence trail and recommendation lineage
- Workflow-specific recommendation policies
- Outcome-linked evaluation data
- Retirement-transition journey depth
- Enterprise trust and controls
- Integration into multiple systems rather than dependence on one platform

---

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|---|---|---:|---|
| Provider | The prototype is hosted through Lovable and does not yet depend on a production LLM provider. A future product would likely use OpenAI, Anthropic, Google, Azure OpenAI, or another managed model provider. No production AI-provider strategy is yet defined. | M | Document the assumed provider stack. Identify which product capabilities require LLM calls and which can use deterministic rules, retrieval, ranking, or workflow logic. Create a provider-dependency map before any production build. |
| Abstraction | There is no production AI gateway, provider-neutral prompt registry, model abstraction layer, or portable recommendation service yet. The product logic is still at prototype stage. | H | Define an AI gateway interface that separates product logic from model calls. Move prompts, schemas, tools, model configuration, and policy checks behind provider-neutral interfaces before scaling. |
| Routing | There is no model-routing policy yet. The product does not yet route tasks by quality, latency, cost, sensitivity, or risk. | H | Create a routing policy that separates low-risk summarization, evidence extraction, recommendation generation, risk-sensitive reasoning, and customer-facing draft generation. Define which tasks can degrade to a lower-cost model or deterministic fallback. |
| Eval | The prototype describes metrics and trust controls, but no automated evaluation suite exists. There is no provider-switch test, golden dataset, recommendation-quality benchmark, or safety regression test yet. | H | Build a small retirement-transition eval set immediately. Include good recommendations, bad recommendations, weak-evidence recommendations, unsafe recommendations, approval-path errors, and outcome-linked cases. Use this eval set before switching or scaling providers. |

---

## Portability Score

Portability Score: **Partial**

The product is not Locked because it is still at prototype stage. It has not yet hard-coded itself into one AI provider, one enterprise platform, one production workflow engine, or one model family.

The product is not Ready because the necessary portability architecture does not yet exist. There is no production AI gateway, routing policy, eval suite, prompt registry, provider-neutral recommendation schema, embedding strategy, tool-calling abstraction, or provider-switch runbook.

Partial is the correct score because the strategy is portable, but the implementation is not yet proven.

The next milestone is to build portability before scale. Relationship Intelligence OS should not enter production until model calls, retrieval, prompts, tools, evidence logging, recommendation policies, human approval, and evals are separated from any single provider.

---

## If the primary AI vendor doubles pricing tomorrow

### 48-hour response plan

If the primary AI vendor doubles pricing tomorrow, the product should not panic-switch providers without evals. The response should protect customer-facing quality, risk controls, and workflow trust first.

### What gets frozen

Freeze the following immediately:

- New high-cost AI features
- Non-essential batch summarization
- Broad exploratory model calls
- Long-context calls without clear business value
- Low-usage prototype workflows
- Any model call not tied to a measured workflow outcome

Do not freeze:

- Human approval workflow
- Evidence logging
- Risk controls
- Recommendation audit trail
- Override-reason capture
- Outcome measurement
- Critical next-best-action workflows already in user testing

### What gets routed differently

Route tasks by value and risk:

| Task Type | 48-Hour Routing Decision |
|---|---|
| Low-risk summarization | Move to lower-cost model or cached summaries |
| Evidence extraction | Use deterministic parsing, retrieval filters, or lower-cost model if evals pass |
| Recommendation generation | Keep on primary model until replacement passes evals |
| Risk-sensitive reasoning | Keep on approved high-quality model with stricter volume control |
| Customer-facing draft language | Keep human approval required; test lower-cost provider only after eval |
| Trend clustering | Batch less frequently; use cheaper model or rules-based clustering |
| Role-lens copy | Cache and reuse; do not regenerate unnecessarily |

### What gets degraded gracefully

Graceful degradation should reduce cost without damaging trust:

- Reduce refresh frequency for non-critical insights
- Cache prior evidence summaries
- Limit long-context reasoning to high-confidence cases
- Show fewer recommendation variants
- Disable low-value exploratory actions
- Use rules-based fallbacks for known workflows
- Keep the approval queue available even if recommendation generation is delayed

### What remains protected

These capabilities should remain protected even under pricing pressure:

- Human approval before customer-visible action
- Evidence trail
- Recommendation lineage
- Risk and suitability boundary checks
- Override-reason capture
- Audit logging
- Customer privacy controls
- Outcome tracking
- Evals before provider switch

### First engineering action

Create a provider-cost control branch with:

- Centralized AI gateway
- Per-task model configuration
- Token and latency logging
- Cache strategy
- Task criticality classification
- Feature flags for provider routing
- Budget threshold alerts

The first engineering move is not replacing the model. It is centralizing control.

### First business communication

Send a concise business update:

- Pricing changed materially.
- Customer-facing quality and risk controls remain protected.
- Non-critical AI workloads are being throttled or routed differently.
- A provider-switch evaluation is underway.
- No customer-visible automation will occur without human approval.
- Business impact will be tracked through cost per approved recommendation, recommendation acceptance rate, override rate, repeat contact, and advisor readiness.

### Metrics to monitor

Track:

- Cost per recommendation shown
- Cost per approved recommendation
- Cost per outcome moved
- Recommendation acceptance rate
- Override rate
- Evidence-open rate
- Latency by workflow
- Model error rate
- Human review burden
- Repeat contact
- Document rework
- Advisor meeting readiness
- Risk-control triggers
- User trust feedback

---

## If the primary AI vendor ships a competing product

If the primary AI vendor ships a competing product, assume they can copy the generic surface quickly.

### What the vendor could copy

A major vendor could copy:

- Generic customer summaries
- AI-generated relationship briefs
- Recommendation cards
- Customer 360 views
- AI assistant UI
- Basic next-best-action workflows
- Chat-based service support
- Generic evidence panels
- Meeting-preparation summaries
- Simple CRM workflow routing
- Basic approval buttons

If Relationship Intelligence OS is only a summary layer, the product is exposed.

### What should remain defensible

The defensible layer must be deeper than the AI interface.

Relationship Intelligence OS should defend through:

- Cross-domain signal model across service, advice, marketing, digital, workplace, operations, documents, and risk
- Human approval / edit / reject history tied to real workflow outcomes
- Role and team preference memory
- Evidence trail with source, timestamp, signal type, and lineage
- Workflow-specific recommendation policies
- Outcome-linked evaluation data
- Retirement-transition journey depth
- Enterprise trust and controls
- Integration into Salesforce, ServiceNow, Microsoft, data platforms, and operational systems
- Ability to act across systems rather than being trapped inside one vendor’s workflow
- Governed learning architecture that separates customer-level, team-level, business-unit-level, and enterprise-level pattern memory

### Defensibility response

The correct response is not to out-feature the vendor’s AI assistant.

The response is to become the trusted action layer for high-value financial-services journeys.

For the Alex Morgan retirement-transition scenario, a vendor may summarize account history or recommend a meeting brief. The defensible version connects:

- Retirement-content engagement
- Mobile behavior
- Workplace contribution activity
- Virtual assistant search
- Secure message
- Service call
- Screen-share support
- Document defect
- Advisor consultation
- Beneficiary status
- Human approval
- Outcome metrics

The product must prove that it can reduce repeat contact, reduce document rework, improve advisor readiness, improve planning coverage, and capture the human feedback that improves the next recommendation.

That is the product’s defense.

---

## 48-Hour Kill Switch Runbook

| Time Window | Product | Engineering | Risk / Controls | Business |
|---|---|---|---|---|
| Hour 0–4 | Freeze non-critical AI features. Identify affected workflows and user-facing risk. Prioritize active recommendation queues. | Disable non-essential model calls through feature flags. Start cost, latency, and error-rate monitoring. Snapshot current prompts, outputs, and logs. | Confirm no customer-visible action can occur without human approval. Review whether any data-boundary or policy issue is triggered. | Notify product, engineering, risk, and business sponsors. State whether this is a pricing, quality, availability, or competitive-response event. |
| Hour 4–12 | Classify workflows into critical, important, and deferrable. Decide which recommendations must remain active. | Route low-risk tasks to cached outputs, lower-cost models, or deterministic fallbacks where safe. Keep high-risk recommendation generation on approved models. | Validate that evidence logging, audit trail, override capture, and approval gates remain intact. | Prepare stakeholder update: what is frozen, what remains protected, what is being tested, and what metrics will govern the response. |
| Hour 12–24 | Review user impact. Confirm that the core recommendation workflow still works for the highest-value journeys. | Run provider-switch evals against the retirement-transition eval set. Compare quality, latency, cost, evidence fidelity, and safety regressions. | Review any quality degradation. Block provider switch for workflows that fail recommendation-quality or safety thresholds. | Communicate early impact: cost change, workflow availability, quality impact, and mitigation plan. |
| Hour 24–48 | Decide whether to continue, degrade, reroute, or pause specific AI workflows. Update product messaging if needed. | Implement temporary routing policy in the AI gateway. Document failure points and permanent architecture gaps. | Approve or reject temporary fallback plan. Confirm auditability and human approval remain intact. | Make the business decision: absorb cost, pass through cost, limit usage, switch provider for specific tasks, or pause non-critical capabilities. |

---

## Minimum Technical Architecture Before Scaling

| Component | Required Portability Standard | Why It Matters |
|---|---|---|
| AI gateway | All model calls must pass through a centralized gateway with provider, model, task, cost, latency, and risk metadata. | Prevents provider lock-in and enables routing, monitoring, fallback, and policy control. |
| Prompt registry | Prompts must be versioned, owned, tested, and stored outside scattered product code. | Allows controlled updates, auditability, regression testing, and provider portability. |
| Model configuration | Model selection must be configuration-driven by task type, risk level, cost, latency, and quality requirement. | Enables switching or routing without rewriting product logic. |
| Retrieval layer | Retrieval logic must be separated from model generation and must log sources used. | Keeps evidence portable and prevents recommendations from depending on a black-box model memory. |
| Embedding strategy | Embeddings should be provider-neutral where possible, with a migration plan for vector stores and embedding models. | Prevents retrieval lock-in and reduces switching cost. |
| Tool/function calling | Tools must use stable internal schemas rather than provider-specific tool formats. | Allows function execution to survive provider changes. |
| Recommendation schema | Recommendations must use a structured schema: saw, inferred, recommends, why, risk, approval, metric. | Makes outputs evaluable, auditable, portable, and easier to validate. |
| Evidence logging | Every recommendation must log source signals, timestamps, evidence opened, and lineage. | Supports trust, compliance, debugging, and future learning. |
| Human approval workflow | Customer-visible actions must require approval, edit, reject, or override capture. | Keeps the product safe for financial-services workflows. |
| Evaluation suite | Evals must test recommendation quality, evidence fidelity, approval-path correctness, unsafe advice, and provider-switch regression. | Provider switching is unsafe without measurable quality gates. |
| Outcome measurement | Recommendations must tie to metrics such as repeat contact, document rework, associate effort, advisor readiness, and planning coverage. | Prevents the product from optimizing AI activity instead of business outcomes. |
| Vendor monitoring | Monitor cost, latency, quality, availability, policy changes, and competitive feature releases by provider. | Makes vendor risk visible before it becomes a crisis. |

---

## Red Lines

Relationship Intelligence OS should not be scaled if any of these conditions are true:

1. Model calls are hard-coded across product code.
2. Prompts are scattered, unversioned, or not testable.
3. There is no automated eval suite for recommendation quality.
4. There is no provider fallback path.
5. There is no evidence logging.
6. There is no human approval before customer-visible action.
7. Override reasons are not captured.
8. Outcome measurement is missing.
9. Recommendation logic is not separated from raw model output.
10. Retrieval sources are not logged.
11. Tool calls depend on provider-specific schemas without abstraction.
12. Role and team preferences are not captured as structured data.
13. Risk controls are implemented as UI copy rather than workflow gates.
14. Customer-sensitive information has no clear data-boundary model.
15. The product cannot degrade gracefully during provider outage or pricing shock.
16. Provider switching cannot be tested before production use.
17. Business users cannot see why a recommendation was made.
18. Risk reviewers cannot audit what evidence was used.
19. Recommendations are approved without knowing which metric should move.
20. The product increases review burden without reducing work.

---

## Next 30-Day Actions

### Week 1: Design AI gateway and recommendation schema

Create the architecture for:

- Centralized AI gateway
- Task taxonomy
- Provider metadata
- Model routing configuration
- Cost and latency tracking
- Recommendation schema
- Evidence schema
- Approval-event schema
- Override-reason taxonomy

The recommendation schema should preserve the core anatomy:

**Saw → Inferred → Recommends → Why → Risk → Approval → Metric**

### Week 2: Move prompts, tools, and model configuration behind provider-neutral interfaces

Create:

- Prompt registry
- Model configuration file
- Tool/function abstraction
- Retrieval interface
- Policy-check interface
- Provider fallback interface
- Feature flags for AI workload routing

No product component should call a model provider directly.

### Week 3: Build eval set for retirement-transition recommendations

Build a human-reviewed eval set using the retirement-transition wedge.

Include:

- Good recommendations
- Bad recommendations
- Weak-evidence recommendations
- Unsafe recommendations
- Over-automation risks
- Wrong approval-path examples
- Missing-context examples
- Hallucinated evidence examples
- Overly broad advice examples
- Recommendations that should be declined

Evaluate:

- Evidence fidelity
- Recommendation specificity
- Risk-boundary correctness
- Approval-path correctness
- Customer-facing language safety
- Outcome linkage
- Provider consistency

### Week 4: Run provider-switch simulation and document failure points

Simulate:

- Primary provider price increase
- Primary provider outage
- Primary provider quality degradation
- Switching summarization to lower-cost model
- Switching evidence extraction to deterministic / lower-cost path
- Keeping high-risk recommendations on approved model
- Failing back to human-only recommendation review

Document:

- Quality loss
- Latency change
- Cost change
- Risk-control failures
- Missing abstraction layers
- Broken prompts
- Broken tools
- Broken evals
- Manual steps required
- Production readiness gaps

---

## Final Assessment

Relationship Intelligence OS is strategically portable only if the team builds the abstraction, routing, eval, and governance layers before production scale.

The product should not compete on model access. It should compete on workflow-specific signal, governed action, and outcome-linked learning.

Current state: **prototype-stage, strategically sound, not yet production-portable.**

Required move before scaling: build the AI gateway, prompt registry, recommendation schema, eval suite, provider-routing policy, evidence logging, and human-approval workflow as first-class architecture.

The strongest kill switch is not the ability to replace one model with another. The strongest kill switch is the ability to preserve the product’s trust, evidence, workflow logic, human approval, and outcome measurement even when the model provider changes.
