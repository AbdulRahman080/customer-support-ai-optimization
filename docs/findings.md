# Findings & Business Case

## Overview

This project analyzed 8,469 customer support tickets across five ticket types and four support channels to identify where operational friction concentrates and to evaluate where AI-assisted workflow improvements would deliver measurable business value.

The analysis focused on:

- Resolution time and response delay patterns
- Customer satisfaction drivers
- Friction and customer effort scoring
- Channel and ticket-type performance
- Product-level support complexity
- AI-assisted triage feasibility and ROI potential

---

# Key Insights

## 1. Support Channel Performance Varies Significantly

Resolution time and satisfaction differ across channels.

Resolution time (slowest → fastest): Social media → Email → Chat → Phone

Customer satisfaction (highest → lowest): Chat → Social media → Email → Phone

### Interpretation

Chat interactions produce the strongest customer experience outcomes and should remain agent-led with AI assistance rather than replaced by automation.

Email and social media interactions show higher friction and represent strong candidates for AI-assisted preprocessing.

Phone support shows lower satisfaction and benefits from optional AI voice-agent support to reduce queue wait time.

---

## 2. Refund Requests Represent the Highest-Friction Ticket Category

Ticket-type friction ranking (highest → lowest): Refund request → Technical issue → Product inquiry → Cancellation request → Billing inquiry

Refund requests showed the highest delay rate, highest friction score, and longest resolution times.

### Interpretation

Refund workflows are strong candidates for automation because they typically follow structured policy-based decision logic. Automating eligibility checks and routing can significantly reduce resolution time and agent workload.

---

## 3. Technical Issues Contribute to Persistent Operational Friction

Technical issue tickets showed high friction scores, moderate delay rates, and lower satisfaction relative to product inquiries and billing inquiries.

### Interpretation

Technical support cases benefit from AI-assisted troubleshooting workflows rather than full automation. Recommended workflow: AI diagnosis → suggested solution → escalation if unresolved.

---

## 4. Priority Labels Alone Do Not Reduce Resolution Time

High-priority tickets had the longest resolution times on average.

Resolution time by priority (slowest → fastest): High → Low → Medium → Critical

### Interpretation

Manual priority classification alone does not reliably accelerate ticket handling. A predictive escalation model based on operational signals — response delay hours, ticket type, channel, customer effort score, and friction score — would improve intervention timing.

---

## 5. Certain Products Generate Higher Support Complexity

Highest friction products: Sony 4K HDR TV, Sony Xperia, Nest Thermostat

These products showed higher average resolution times, lower satisfaction scores, and higher friction scores — likely due to configuration complexity and compatibility issues. AI-assisted troubleshooting workflows can reduce resolution time for these categories.

---

# AI Workflow Findings

AI-assisted ticket summarization and classification using the Gemini API demonstrated strong potential for improving triage efficiency when paired with validation logic.

Observed benefits: reduced agent reading effort, faster issue understanding, consistent ticket categorization, and routing recommendations aligned with business categories.

Observed limitations: ambiguity in overlapping issue categories, sensitivity to incomplete ticket descriptions, and the need for confidence-based validation before full automation.

### Operational Recommendation

AI should be deployed as a triage support layer, not as an agent replacement.

Recommended workflow:
1. Generate ticket summary
2. Predict ticket category
3. Predict urgency
4. Recommend routing queue
5. Escalate low-confidence cases for manual review

---

# Business Case & ROI Estimates

The following estimates are based on industry benchmarks for mid-size customer support operations and the friction patterns observed in this dataset. They are intended as directional inputs for a business case conversation, not precise forecasts.

## Baseline Assumptions

| Parameter | Assumed Value | Basis |
|---|---|---|
| Monthly ticket volume | ~8,500 tickets | Dataset size as monthly proxy |
| Average handle time per ticket (manual triage) | 8 minutes | Industry benchmark, inbound support |
| Average hourly agent cost (fully loaded) | $35/hr | Mid-market support centre estimate |
| Average resolution time (current state) | ~168 hours | Derived from dataset |
| Customer satisfaction scale | 1–5 | Dataset |

---

## Initiative 1: AI-Assisted Triage for Email and Social Media

**Target:** Email (25% of volume) and social media (25% of volume) — highest friction channels.

AI preprocessing reduces triage time by summarizing tickets, predicting category and urgency, and recommending the routing queue before an agent touches the ticket.

| Metric | Estimate |
|---|---|
| Tickets affected monthly | ~4,250 (50% of volume) |
| Expected handle time reduction per ticket | 2–3 minutes |
| Monthly agent hours saved | 142–213 hours |
| Monthly cost saving (at $35/hr) | **$4,970 – $7,455** |
| Annual cost saving | **$59,640 – $89,460** |

**Additional benefit:** Faster first response and more consistent routing reduces delay rates in the two highest-friction channels, with expected knock-on improvement to satisfaction scores.

---

## Initiative 2: Refund and Cancellation Automation

**Target:** Refund requests (~20% of volume) and cancellation requests (~20% of volume).

These ticket types follow rule-based decision logic — eligibility check, policy validation, approval or escalation. Automating routine approvals removes agent handling entirely for qualifying cases.

Conservative assumption: 40% of refund/cancellation tickets qualify for full automation under standard policy.

| Metric | Estimate |
|---|---|
| Tickets affected monthly | ~3,400 (40% of refund/cancellation volume) |
| Agent time eliminated per ticket | 8 minutes (full handle time) |
| Monthly agent hours saved | ~453 hours |
| Monthly cost saving | **$15,867** |
| Annual cost saving | **$190,400** |

**Additional benefit:** Resolution time for automated cases drops from ~168 hours average to near-instant for eligible cases, directly improving satisfaction for the highest-friction ticket category.

---

## Initiative 3: Escalation Prediction Layer

**Target:** High-risk tickets currently misclassified by manual priority labels.

The analysis showed that High-priority tickets had longer resolution times than Critical tickets — indicating that the current labeling system is not reliably identifying urgent cases. A predictive model using resolution delay indicators, ticket type, channel, customer effort score, and friction score would enable earlier intervention.

| Metric | Estimate |
|---|---|
| Tickets at risk of SLA breach (estimated) | ~15% of monthly volume (~1,275) |
| Reduction in SLA breach rate (conservative) | 25–30% |
| Tickets saved from breach monthly | ~320–380 |
| Value per prevented breach (SLA penalty or churn cost) | $50–$150 per ticket (context-dependent) |
| Monthly value recovered | **$16,000 – $57,000** |
| Annual value recovered | **$192,000 – $684,000** |

The wide range reflects uncertainty in churn cost per breach. Even the conservative end represents substantial value recovery.

---

## Combined ROI Summary

| Initiative | Annual Value (Low) | Annual Value (High) |
|---|---|---|
| Email / social triage automation | $59,640 | $89,460 |
| Refund / cancellation automation | $190,400 | $190,400 |
| Escalation prediction layer | $192,000 | $684,000 |
| **Total** | **$442,040** | **$963,860** |

Estimated implementation cost for a mid-size operation (API costs, integration, QA): $40,000–$80,000 one-time, with ongoing API costs of approximately $5,000–$15,000/year at scale.

**Payback period (conservative estimate): 3–5 months.**

---

## Important Caveats

These estimates are directional. Actual results depend on:

- Current manual handle time (will vary by team)
- Agent headcount and fully loaded cost
- Automation eligibility rate for refund/cancellation (policy-dependent)
- AI classification accuracy on production ticket data
- Integration complexity with existing helpdesk tooling (Zendesk, Freshdesk, etc.)

A 60-day pilot on email and refund tickets — with proper pre/post measurement — would validate these assumptions before broader rollout.

---

# Channel-Specific Automation Strategy

## Phone Channel

Introduce optional AI voice-agent support. Customers choose between AI agent (fast) or human agent (traditional queue).

AI handles: billing questions, refund status checks, cancellation requests, product compatibility questions. Complex cases escalate automatically.

Expected impact: reduced queue time, improved accessibility, higher resolution speed.

## Chat Channel

Chat already produces the highest satisfaction outcomes. Keep human-agent workflow.

Add: AI summarization assistance, response suggestion support, routing hints.

Expected impact: improved agent efficiency without reducing service quality.

## Email and Social Media Channels

AI summary → AI classification → urgency prediction → routing recommendation.

Confidence-based logic: high confidence → auto-route; low confidence → manual review.

Expected impact: reduced triage time, improved routing consistency, lower resolution delays.

## Refund and Cancellation Automation Pipeline

AI detects request type → eligibility rules applied → auto-approval when policy conditions met → manual review for exceptions only.

Expected impact: lower resolution time, reduced escalation workload, improved customer experience.

## Technical Issue Support Workflow

AI identifies issue → AI suggests resolution steps → escalate unresolved cases.

Expected impact: reduced agent workload, faster first-response quality, improved resolution speed.

## Escalation Prediction Layer

Predict escalation risk using: resolution delay indicators, ticket type, channel, customer effort score, friction score.

Expected impact: earlier intervention, improved SLA performance, reduced long-tail delays.

---

# Business Impact Summary

This project demonstrates how customer operations teams can use analytics and AI-assisted workflows to reduce friction across the support lifecycle.

The data shows clear, actionable targets: email and social media triage, refund/cancellation automation, and predictive escalation. Each initiative has a measurable cost driver and a plausible path to positive ROI within the first year.

The proposed workflow balances automation efficiency with human oversight and aligns with modern AI-enabled customer operations strategies.
