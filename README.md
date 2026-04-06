# Customer Experience Optimization with AI-Assisted Ticket Triage

## 1. Problem

Customer support inefficiencies can create delays, increase agent workload, and lead to poor customer experience. Manual triage often requires agents to read long ticket descriptions, determine issue type, assign urgency, and route cases manually. This process can be inconsistent and slow, especially when ticket volume increases.

This project explores how data analysis and AI-assisted workflows can reduce friction across the support lifecycle.

---

## 2. Solution

This project combines customer support analytics with AI-assisted triage design to identify operational bottlenecks and evaluate workflow improvements.

Using support ticket data, the project:
- measures friction across ticket types and channels
- identifies delay and satisfaction patterns
- evaluates Gemini-based ticket summarization and classification
- redesigns the triage workflow to support faster, more consistent handling

---

## 3. Key Features

### Dashboard Analysis
- KPI reporting for ticket handling performance
- resolution time and response delay analysis
- customer satisfaction trends
- channel and ticket-type comparisons

### Friction Identification
- dynamic delay detection
- customer effort scoring
- high-friction ticket analysis
- prioritization of operational bottlenecks

### AI Summaries and Classification
- Gemini-generated ticket summaries
- AI classification into support categories
- urgency prediction and routing recommendations
- validation of AI outputs against ticket labels

### Workflow Redesign
- current-state vs future-state support process
- AI-assisted triage workflow design
- confidence-based manual review logic
- business requirements documentation

---

## 4. Results

The project identified key support workflow bottlenecks and showed how AI can improve triage efficiency when paired with validation and review logic.

### Main outcomes
- identified high-friction ticket categories
- showed that longer resolution time is associated with lower customer satisfaction
- created a customer effort score to flag difficult experiences
- demonstrated that AI can reduce manual triage effort through summaries and routing suggestions
- designed a workflow that combines automation with human review for safer operational use

---

## Repository Structure

```text
customer-experience-ai-optimization/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 1_data_cleaning.ipynb
│   ├── 2_kpi_dashboard.ipynb
│   ├── 3_friction_analysis.ipynb
│   └── 4_ai_workflow.ipynb
│
├── docs/
│   ├── workflow_design.md
│   ├── requirements.md
│   └── findings.md
│
├── visuals/
│   └── workflow_diagram.png
│
└── README.md
