# Findings

## Overview

This project analyzed customer support ticket data to identify operational friction across support channels and ticket categories, and to evaluate where AI-assisted workflow improvements could reduce resolution time and improve customer experience.

The analysis focused on:

- resolution time
- customer satisfaction
- delay rate
- friction score
- channel performance
- ticket category performance
- product-level support complexity
- opportunities for AI-assisted triage automation

The goal was to identify practical workflow improvements aligned with modern customer operations environments.

---

# Key Insights

## 1. Support Channel Performance Varies Significantly

Resolution time and satisfaction differ across channels.

Observed ordering:

Resolution time (highest → lowest)

Social media  
Email  
Chat  
Phone

Customer satisfaction (highest → lowest)

Chat  
Social media  
Email  
Phone

### Interpretation

Chat interactions produce the strongest customer experience outcomes and should remain agent-led with AI assistance rather than replaced by automation.

Email and social media interactions show higher friction and represent strong candidates for AI-assisted preprocessing.

Phone support shows lower satisfaction and benefits from optional AI voice-agent support to reduce queue wait time.

---

## 2. Refund Requests Represent the Highest-Friction Ticket Category

Ticket-type friction ranking:

Refund request  
Technical issue  
Product inquiry  
Cancellation request  
Billing inquiry

Refund requests showed:

- highest delay rate
- highest friction score
- longest resolution times

### Interpretation

Refund workflows are strong candidates for automation because they typically follow structured policy-based decision logic.

Automating eligibility checks and routing can significantly reduce resolution time and agent workload.

---

## 3. Technical Issues Contribute to Persistent Operational Friction

Technical issue tickets showed:

- high friction score
- moderate delay rate
- lower satisfaction relative to product inquiries and billing inquiries

### Interpretation

Technical support cases benefit from AI-assisted troubleshooting workflows rather than full automation.

Recommended workflow:

AI diagnosis → suggested solution → escalation if unresolved

This reduces workload while preserving resolution quality.

---

## 4. Product Inquiry and Billing Inquiry Tickets Show High Satisfaction but Still Benefit from Automation

Observed characteristics:

- strong satisfaction outcomes
- moderate resolution times
- moderate delay rates

### Interpretation

These ticket types are strong candidates for AI-assisted routing and automated response generation.

Automation here improves speed without increasing risk.

---

## 5. Priority Labels Alone Do Not Reduce Resolution Time

Analysis showed:

High-priority tickets had the longest resolution times on average.

Priority ordering by resolution time:

High  
Low  
Medium  
Critical

### Interpretation

Manual priority classification alone does not reliably accelerate ticket handling.

A predictive escalation model based on operational signals would improve intervention timing.

Recommended predictors:

- response delay hours
- ticket type
- channel
- customer effort score
- friction score

---

## 6. Channel Friction Patterns Suggest Email Should Be the First Automation Target

Channel friction ranking:

Email  
Phone  
Social media  
Chat

Chat produced the highest satisfaction scores and lowest friction scores.

Email produced the highest friction score overall.

### Interpretation

Email tickets benefit most from AI-assisted preprocessing including:

- summarization
- classification
- routing recommendation
- urgency prediction

---

## 7. Certain Products Generate Higher Support Complexity

Highest friction products:

Sony 4K HDR TV  
Sony Xperia  
Nest Thermostat

These products showed:

- higher average resolution times
- lower satisfaction scores
- higher friction scores

### Interpretation

These products likely involve configuration complexity and compatibility issues.

AI-assisted troubleshooting workflows can reduce resolution time for these categories.

---

# AI Workflow Findings

AI-assisted ticket summarization and classification using Gemini demonstrated strong potential for improving triage efficiency when paired with validation logic.

Observed benefits:

- reduced agent reading effort
- faster issue understanding
- consistent ticket categorization support
- routing recommendations aligned with business categories

Observed limitations:

- ambiguity in overlapping issue categories
- sensitivity to incomplete ticket descriptions
- need for confidence-based validation before automation

### Operational Recommendation

AI should be deployed as a triage support layer rather than a replacement for agents.

Recommended workflow:

1. generate ticket summary
2. predict category
3. predict urgency
4. recommend routing queue
5. escalate low-confidence cases for manual review

---

# Channel-Specific Automation Strategy

Based on friction analysis results, a hybrid automation architecture is recommended.

## Phone Channel

Introduce optional AI voice-agent support.

Customers choose:

AI agent (fast support)  
Human agent (traditional queue)

AI handles:

- billing questions
- refund status checks
- cancellation requests
- product compatibility questions

Complex cases escalate automatically.

Expected impact:

Reduced queue time  
Improved accessibility  
Higher resolution speed

---

## Chat Channel

Chat already produces the highest satisfaction outcomes.

Recommended approach:

Keep human-agent workflow

Add:

AI summarization assistance  
response suggestion support  
routing hints

Expected impact:

Improved agent efficiency without reducing service quality

---

## Email and Social Media Channels

Email and social channels show the highest friction scores.

Recommended workflow:

AI summary  
AI classification  
urgency prediction  
routing recommendation

Confidence-based logic:

High confidence → auto-route  
Low confidence → manual review

Expected impact:

Reduced triage time  
Improved routing consistency  
Lower resolution delays

---

## Refund and Cancellation Automation Pipeline

Refund and cancellation workflows are strong candidates for automation.

Recommended process:

AI detects request type  
Eligibility rules applied  
Auto-approval when policy conditions are met  
Manual review only for exceptions

Expected impact:

Lower resolution time  
Reduced escalation workload  
Improved customer experience

---

## Technical Issue Support Workflow

Technical issue tickets benefit from assisted troubleshooting rather than full automation.

Recommended process:

AI identifies issue  
AI suggests resolution steps  
Escalate unresolved cases

Expected impact:

Reduced agent workload  
Faster first-response quality  
Improved resolution speed

---

## Escalation Prediction Layer

Priority labels alone did not reliably predict faster resolution outcomes.

Recommended solution:

Predict escalation risk using:

resolution delay indicators  
ticket type  
channel  
customer effort score  
friction score

Expected impact:

Earlier intervention  
improved SLA performance  
reduced long-tail delays

---

# Business Impact

This project demonstrates how customer operations teams can use analytics and AI-assisted workflows to reduce friction across the support lifecycle.

Expected improvements include:

reduced manual triage effort  
faster routing decisions  
lower delay rates  
improved resolution consistency  
earlier escalation detection  
better support experience across channels

The proposed workflow balances automation efficiency with human oversight and aligns with modern AI-enabled customer operations strategies.
