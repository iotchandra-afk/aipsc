# Data Flywheel Map

## Product

Product: Relationship Intelligence OS

## Core Moat Thesis

Relationship Intelligence OS becomes defensible only if usage creates proprietary signal that improves future recommendations.

The moat is not access to customer, service, marketing, operations, digital, risk, and relationship data. Large enterprises already have that data, and large platforms can increasingly summarize it.

The moat is the feedback loop created when humans review AI recommendations inside real work:

**Signals observed → inference made → action recommended → human approved / edited / rejected → outcome measured → future recommendation improved**

The product must get better every time a relationship manager, service associate, advisor, marketer, operations leader, or risk reviewer interacts with a recommendation.

The product should not rely on retraining a foundation model as the primary learning mechanism. The enterprise-safe learning loop should improve through structured feedback, ranking, retrieval, rules, evaluation datasets, preference profiles, and governed recommendation policies.

---

## What Is Proprietary

### Data the product consumes

Relationship Intelligence OS consumes signals from:

- Customer profile and household context
- Service cases and repeat-contact history
- Digital and mobile behavior
- Secure messages and virtual assistant searches
- Advisor meetings and relationship-manager activity
- Marketing engagement
- Workplace benefits activity
- Document defects and operational workflows
- Risk controls and approval history
- Outcome metrics such as rework, repeat contact, meeting readiness, and planning coverage

These inputs are valuable, but they are not enough to create a moat.

### Signal the product creates

The proprietary signal is created through use:

- Which recommendations users approve
- Which recommendations users edit
- Which recommendations users reject
- Which evidence users inspect before approving
- Which action-bundle items users remove or add
- Which recommendations are escalated
- Which override reasons appear repeatedly
- Which risk controls block customer-visible action
- Which recommendations move real business metrics
- Which role-specific preferences emerge over time

That created signal is harder for a platform competitor to copy because it reflects human judgment, workflow context, domain practice, and outcome feedback.

---

## Flywheel Loops

| Loop | What It Measures | Score |
|---|---|---:|
| Correction | Do users fix AI outputs, and is that signal captured for reuse? | 3/5 |
| Preference | Does the product learn role, team, and workflow preferences over time? | 2/5 |
| Domain Context | Does usage in one domain improve quality in adjacent domains? | 4/5 |
| Network | Does each new user, team, or workflow make the product better for others? | 3/5 |

Total Flywheel Score: **12/20**

Weakest Loop: **Preference Loop**

The weakest loop is Preference because the prototype shows role lenses, but does not yet prove persistent preference learning. This is the first loop to fix because platform competitors can attack by embedding preference learning directly inside CRM, service, productivity, and workflow systems.

---

## Loop 1: Correction Loop — 3/5

### What is captured today

The prototype shows a credible correction loop through:

- Approve action
- Request changes
- Decline
- Override-reason capture
- Action-bundle checkboxes
- Evidence chips
- Risk guardrails
- Human approval status
- Metric-to-move panel

This means the product can capture whether a recommendation was trusted, modified, rejected, or escalated.

### Why it matters

Corrections become proprietary evaluation data.

If users repeatedly remove a suggested action, that action should be demoted in similar journeys. If service associates repeatedly add missing-document outreach, the product should learn that document defects are stronger predictors of repeat contact than case type alone. If risk reviewers frequently reject actions lacking policy evidence, the product should require stronger evidence before surfacing similar recommendations.

### What must be instrumented

Every recommendation should create a structured feedback event:

- Recommendation ID
- Customer / household context
- Journey type
- Signals used
- Evidence opened
- Action bundle shown
- Action bundle edited
- Approval decision
- Override reason
- Role of reviewer
- Risk flags
- Outcome metric expected to move
- Outcome metric actually moved

### Why this is not a 5

The prototype shows the interaction design, but not the production learning system. To become a true moat, the product needs instrumentation, feedback schema, evaluation datasets, governance review, and safe reuse rules.

---

## Loop 2: Preference Loop — 2/5

### What is captured today

The prototype includes role lenses for:

- Relationship Manager
- Service Associate
- Advisor / Wealth Team
- Marketing Partner
- Operations Leader
- Risk Reviewer
- Executive Leader

This proves that the same intelligence should be interpreted differently by role.

However, the product does not yet prove persistent preference learning.

### Missing preference memory

The product needs to learn:

- Which evidence types each role trusts
- Which actions each team approves quickly
- Which actions supervisors reject
- Which recommendation formats users prefer
- Which workflows need stricter approval gates
- Which customer segments require different handling
- Which journeys require more conservative action
- Which business units require different escalation thresholds

### Why this matters

Preference learning is where the product becomes hard to displace.

A relationship manager may care most about proactive outreach. A service associate may care most about missing information. An advisor may care most about meeting preparation. A marketing partner may care about campaign-to-service impact. A risk reviewer may care about evidence lineage and approval status.

If the product remembers those patterns, future recommendations become faster, sharper, and more trusted.

### First fix

Create a governed preference model with four layers:

1. **Role preference** — what each role needs from the recommendation
2. **Team preference** — how each team routes, approves, or edits actions
3. **Workflow preference** — how each journey type should be handled
4. **Risk preference** — which actions require stricter review

Every approval, edit, rejection, reassignment, and override should update the relevant preference profile.

### Why this is the weakest loop

The prototype shows role-specific framing, but not durable preference memory. A platform competitor such as Salesforce, Microsoft, or ServiceNow could attack this loop by learning preferences inside the workflow where users already work.

---

## Loop 3: Domain Context Loop — 4/5

### What is captured today

This is the strongest loop.

The Alex Morgan scenario connects signals across:

- Digital content behavior
- Mobile usage
- Workplace 401(k) activity
- Virtual assistant search
- Marketing engagement
- Document defect
- Secure message
- Service call
- Screen-share support
- Advisor consultation
- Reopened case
- Risk approval requirement

The product’s value comes from connecting these signals into one retirement-transition interpretation.

### Why it matters

The product becomes more valuable when activity in one domain improves action in another.

Examples:

- Marketing engagement predicts service demand.
- Document defects predict repeat contact.
- Virtual assistant searches predict future call volume.
- Workplace contribution behavior predicts advice readiness.
- Service friction predicts relationship risk.
- Advisor meetings change the urgency of case resolution.
- Risk reviews improve future approval routing.
- Digital behavior surfaces a relationship moment before a formal case arrives.

### How it compounds

Over time, the product can learn journey patterns such as:

- Retirement transition
- Beneficiary update
- Rollover / consolidation
- Required minimum distribution
- Cash transfer concern
- Account access friction
- Document defect
- Market-volatility service demand

Each journey pattern improves future recommendations, evidence requirements, routing, and approval logic.

### Why this is not a 5

The prototype shows cross-domain reasoning, but does not yet prove production-scale learning across business units, teams, customer segments, and workflows.

---

## Loop 4: Network Loop — 3/5

### What is captured today

The product has a plausible network loop because each new team can contribute:

- More reviewed recommendations
- More override reasons
- More evidence patterns
- More journey examples
- More segment-specific outcomes
- More service-to-marketing causality
- More operational defect patterns
- More risk-control feedback

### Why it matters

Each new workflow should improve the product’s understanding of common relationship journeys.

Examples:

- Beneficiary update journeys often create rework.
- Rollover journeys often require proactive checklisting.
- Retirement-content engagement can precede service demand.
- Document upload defects raise repeat-contact risk.
- Marketing campaigns can create unplanned service volume.
- Advisor meetings are more effective when service issues are cleared beforehand.

### Enterprise limitation

The network loop is constrained by privacy, permissioning, business-unit boundaries, regulatory controls, and customer-data restrictions.

The product cannot casually learn from every user and apply that learning everywhere. It needs a governed learning architecture.

### Governed learning architecture

The product should separate learning into four layers:

1. **Customer-level memory** — private to a customer or household
2. **Team-level memory** — preferences and workflow patterns for a team
3. **Business-unit-level memory** — patterns reusable within a business area
4. **Enterprise-level pattern memory** — anonymized journey intelligence approved for broader reuse

This is what makes the network loop enterprise-safe.

---

## Moat Strength Summary

| Dimension | Assessment |
|---|---|
| Strongest loop | Domain Context |
| Weakest loop | Preference |
| Most urgent fix | Structured preference model |
| Most valuable created signal | Human approval / edit / reject behavior tied to outcomes |
| Most dangerous competitor move | Native workflow platforms learning preferences inside existing systems |
| Best defense | Own the cross-domain action loop, not the summary layer |

---

## Encroachment Threat Assessment

### Threat 1: Salesforce Agentforce / Einstein / Data Cloud

Attack vector:

Salesforce ships a native relationship-moment assistant inside CRM and Service Cloud. It summarizes customer history, detects next-best actions, routes work through Salesforce Flow, and learns approval preferences directly inside the system where sales and service users already work.

Time-to-threat: **3–6 months**

Value at risk: **55%**

Why this is dangerous:

Salesforce already owns CRM workflow placement in many enterprises. If Relationship Intelligence OS is only a summary layer or recommendation card, Salesforce can compress it into a native feature.

Defense:

Do not compete as a CRM assistant. Compete as the cross-domain action layer connecting service, advice, marketing, digital, workplace, operations, document defects, risk, and outcome feedback.

---

### Threat 2: Microsoft Copilot

Attack vector:

Microsoft uses email, Teams, calendar, documents, meetings, and enterprise graph data to create a broad productivity intelligence layer. It may not go as deep into financial-services workflows, but it can own the daily work surface.

Time-to-threat: **3–9 months**

Value at risk: **35%**

Why this is dangerous:

Microsoft has workflow gravity. If recommendations, meeting briefs, customer summaries, and task routing appear naturally in Outlook, Teams, and Office, users may not want another destination.

Defense:

Relationship Intelligence OS must integrate into Microsoft surfaces while owning the domain-specific recommendation logic, evidence model, approval workflow, and business-outcome feedback loop.

---

### Threat 3: ServiceNow Now Assist / Financial Services Operations

Attack vector:

ServiceNow expands from service operations into relationship intelligence by connecting cases, workflows, knowledge, approvals, and operational service patterns.

Time-to-threat: **6–9 months**

Value at risk: **40%**

Why this is dangerous:

ServiceNow can own operational workflow, case routing, approval flows, and service productivity. It can frame an external intelligence layer as unnecessary.

Defense:

Relationship Intelligence OS must avoid being reduced to service operations. It must prove cross-domain intelligence across service, advice, marketing, digital behavior, workplace activity, document defects, risk, and measurable outcomes.

---

### Threat 4: Focused Wealth-Tech / Retirement AI Startup

Attack vector:

A focused startup builds deeply for retirement-transition journeys: rollover, beneficiary cleanup, retirement-income planning, advisor meeting preparation, document defect repair, and proactive outreach.

Time-to-threat: **6–12 months**

Value at risk: **30%**

Why this is dangerous:

A vertical competitor could be sharper in the first wedge. It may win by being narrower, faster, and more purpose-built.

Defense:

Use retirement transition as the first wedge. Go deep before expanding. Capture proprietary journey signal, document-defect patterns, advisor-preparation outcomes, and service-rework reduction.

---

## 90-Day Encroachment Plan

Attacker: Salesforce Agentforce / Einstein / Data Cloud

Targeted weak loop: **Preference Loop**

Salesforce attacks by embedding preference learning directly into CRM and Service Cloud. It learns which next-best actions each role, team, and manager approves or rejects, then uses native workflow placement to make Relationship Intelligence OS feel external.

### Days 1–30: Ship the native feature

Salesforce ships a “Relationship Moment Assistant” inside CRM and Service Cloud.

It includes:

- Customer 360 summary
- Service-history summary
- Next-best-action card
- Approval workflow
- Saved team preferences
- Salesforce Flow integration
- Agentforce action routing
- CRM-native evidence trail
- Admin-configurable recommendation rules

The feature does not need to be better. It only needs to be native and close enough.

### Days 31–60: Win the workflow argument

Salesforce targets CRM admins, service leaders, relationship managers, and procurement teams with a simple message:

“You already have the data, workflow, permissions, and users in Salesforce. Why add another layer?”

Salesforce offers:

- Lower implementation friction
- Existing permission model
- Familiar admin controls
- Native CRM workflow
- Packaged templates
- Bundled pricing
- Easier procurement path

### Days 61–90: Make switching back painful

Users do not come back if:

- Approval history stays inside Salesforce
- Team preferences are configured by Salesforce admins
- Recommendations are embedded inside daily workflow
- Procurement rejects another AI vendor
- Managers prefer a bundled platform feature
- Users do not want another destination

### Defense Plan

Relationship Intelligence OS must defend by doing what a single workflow platform cannot easily do:

1. Capture approval, edit, rejection, override, and routing behavior as structured product signal.
2. Build the preference loop immediately.
3. Prove that cross-domain signals predict outcomes CRM-only data misses.
4. Start with a deep retirement-transition wedge.
5. Integrate into Salesforce, ServiceNow, and Microsoft surfaces rather than forcing users into another destination.
6. Own the recommendation logic, evidence model, trust controls, and outcome feedback loop.
7. Create role-specific recommendation memory for service, advisor, marketing, operations, risk, and executive users.
8. Build human-reviewed evaluation datasets.
9. Measure business impact through repeat contact, document rework, associate effort, advisor readiness, planning coverage, and override quality.
10. Turn every human correction into the next version of the moat.

---

## Next 30-Day Moat Build Plan

The product should not wait for scale to build the moat. The first 30 days should instrument the learning loop.

### Week 1: Define feedback schema

Create structured events for:

- Recommendation shown
- Evidence opened
- Action approved
- Action edited
- Action rejected
- Action routed
- Override reason submitted
- Risk control triggered
- Outcome metric observed

### Week 2: Build preference objects

Create preference objects for:

- Role
- Team
- Workflow
- Customer segment
- Risk threshold
- Evidence depth
- Approval pattern

### Week 3: Build evaluation set

Create a human-reviewed evaluation set for the retirement-transition journey.

Include:

- Good recommendations
- Bad recommendations
- Unsafe recommendations
- Weak-evidence recommendations
- Missing-context recommendations
- Over-automation risks
- Correct approval paths

### Week 4: Connect outcomes

Tie recommendations to outcome metrics:

- First-touch resolution
- Repeat contact
- Document rework
- Associate effort
- Advisor meeting readiness
- Planning coverage
- Risk defect avoidance
- Override rate
- Recommendation acceptance rate

---

## Kill / Narrow Signals

The moat should be considered weak if any of these are true after early testing:

1. Users approve or reject recommendations without opening evidence.
2. Override reasons are vague or not captured.
3. Recommendations do not change based on prior corrections.
4. Role lenses remain cosmetic rather than changing action logic.
5. The product cannot show outcome movement.
6. Users describe the product as a dashboard or summary layer.
7. The strongest signals already live entirely inside Salesforce, Microsoft, or ServiceNow.
8. The product cannot integrate into existing workflows.
9. Risk and approval controls slow the product without improving trust.
10. The product creates more review burden than work reduction.
