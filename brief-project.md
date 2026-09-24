# [PROJECT NAME]: DATA PROJECT BRIEF

**Document Status:** [Draft / Under Review / Approved]

**Project Owner:** [Your Name, Title]

**Target Completion Date:** [YYYY-MM-DD]

**Version:** 1.0

---

## EXECUTIVE SUMMARY

*(Write this section last. Provide a 3–4 sentence "Elevator Pitch" summarizing the business background, the technical data approach, the expected deliverable, and the anticipated business impact.)*

> **Example:** Recent changes in user acquisition channels have led to a 15% drop in 30-day subscriber retention. This project will build a diagnostic data pipeline and an interactive Power BI dashboard to identify key drop-off drivers across user cohorts. Delivering this project will enable the product marketing team to launch automated retention triggers, targeting a recovery of $80,000 in monthly recurring revenue.

---

## 1. BUSINESS UNDERSTANDING

### 1.1 Business Context & Problem Statement

* **Current Situation:** [Describe the current state of business operations or existing workflows.]
* **Core Problem:** [What specific pain point, operational inefficiency, or lack of visibility needs to be solved?]
* **Key Business Hypotheses to Test:**
* *Hypothesis 1:* [e.g., Customers who do not complete profile onboarding within 48 hours churn at double the baseline rate.]
* *Hypothesis 2:* [e.g., Mobile app users experience a 30% higher checkout failure rate during peak evening hours.]



### 1.2 Objectives & Success Criteria Alignment

| Dimension | Description | Success Criteria / Target Metric |
| --- | --- | --- |
| **Business Objective** | [What the organization wants to achieve commercially] | [e.g., Reduce 90-day subscriber churn from 12% to 8%] |
| **Data Mining / Analytics Goal** | [The technical data science task to be performed] | [e.g., Binary classification predicting 60-day cancellation risk] |
| **Technical Success Criteria** | [Algorithmic or data pipeline evaluation benchmark] | [e.g., Model ROC-AUC $\ge 0.80$; pipeline runtime $< 15$ minutes] |

---

## 2. STAKEHOLDER & PERSONNEL MATRIX

Because this project is executed by a solo data professional, clear classification of external stakeholders is critical to protect bandwidth and decision-making authority.

| Name | Organizational Title | CRISP-DM / Brief Role | Engagement & Responsibility |
| --- | --- | --- | --- |
| **[Name]** | [e.g., VP of Marketing] | **Approver** | Signs off on scope, wireframes, budget, and final project delivery. |
| **[Your Name]** | Lead Data Analyst / Scientist | **Contributor (Owner)** | Executes all CRISP-DM phases (Data prep, modeling, reporting, deployment). |
| **[Name]** | [e.g., Lead Data Engineer] | **Contributor (Advisory)** | Provides database access credentials, schema guidance, and infrastructure support. |
| **[Name]** | [e.g., Support Team Leads] | **Informee** | Receives bi-weekly status updates; no direct sign-off authority. |

---

## 3. DATA UNDERSTANDING & INFRASTRUCTURE

### 3.1 Data Sources & Resource Inventory

* **Source Systems Required:** [e.g., PostgreSQL production database, Google Analytics 4 clickstream data, Zendesk API]
* **Target Analytical Storage:** [e.g., Snowflake, BigQuery, local DuckDB instance]
* **Target Tools & Tech Stack:** [e.g., dbt, Python (pandas/scikit-learn), Power BI, Docker]

### 3.2 Data Quality, Assumptions & Constraints

* **Known Quality Issues:** [e.g., Historic user survey responses contain ~20% missing values; location fields require standardization.]
* **Technical Constraints:** [e.g., Clickstream event logs are only retained for 90 days in raw storage.]
* **Risks & Contingency Plan:**
* *Risk:* [Primary key mismatch between web logs and CRM user IDs.]
* *Contingency:* [Fallback to deterministic email-address and timestamp matching during Phase 3 (Data Preparation).]



---

## 4. SCOPE & EXPECTED DELIVERABLES

### 4.1 Deliverable Artifacts

1. **Primary Output:** [e.g., Interactive Power BI Dashboard refreshed daily at 6:00 AM UTC]
2. **Technical Pipeline:** [e.g., Tested and documented dbt data transformation models in Snowflake]
3. **Executive Presentation:** [e.g., 10-slide summary deck detailing churn drivers and recommended product actions]

### 4.2 Deliverable Wireframe / Report Skeleton

*(Attach or link a visual sketch, whiteboard wireframe, or table layout approved by the Approver before coding starts.)*

* **Wireframe / Design Link:** `[Insert Link to Figma / Excalidraw / Whiteboard Sketch]`
* **Core Layout Notes:**
* *Header:* High-level KPI cards (Total Active Subscribers, Current Churn Rate, Projected LTV Impact).
* *Main Visual:* Monthly cohort retention heatmap filtered by acquisition channel and region.
* *Drill-Down:* Customer-level risk scoring table with direct links to CRM profiles.



### 4.3 Scope Boundaries (Preventing Scope Creep)

* **IN-SCOPE:**
* Analysis restricted to registered users in North America and European regions.
* Historical transaction analysis covering the past 12 months.


* **OUT-OF-SCOPE:**
* Building real-time streaming pipelines (batch processing is sufficient).
* Integrating predictive API scores directly into external third-party email tools (Phase 2 initiative).



---

## 5. PROJECT PLAN, MILESTONES & CONTINGENCY

Workflows follow the six iterative phases of the CRISP-DM lifecycle, tailored for a solo contributor.

```
┌──────────────────────────────────────────────────────────────────────────────────┐
│                             CRISP-DM PROJECT TIMELINE                            │
├───────────────┬───────────────┬───────────────┬───────────────┬──────────────────┤
│ Phase 1 & 2   │ Phase 3       │ Phase 4       │ Phase 5       │ Phase 6          │
│ Business &    │ Data          │ Modeling &    │ Business      │ Deployment &     │
│ Data Und.     │ Preparation   │ Analytics     │ Evaluation    │ Final Review     │
└───────────────┴───────────────┴───────────────┴───────────────┴──────────────────┘

```

| CRISP-DM Phase | Target Checkpoint Output | Estimated Completion |
| --- | --- | --- |
| **1. Business & Data Understanding** | Signed Project Brief; initial Data Quality & Dictionary Audit. | [YYYY-MM-DD] |
| **2. Data Preparation** | Cleaned, transformed, and merged datasets (dbt / SQL / Python scripts). | [YYYY-MM-DD] |
| **3. Modeling & Analysis** | Executed models/queries, validated accuracy, wireframe populated. | [YYYY-MM-DD] |
| **4. Evaluation** | Review meeting with **Approver** to evaluate output against business KPIs. | [YYYY-MM-DD] |
| **5. Deployment** | Production dashboard published; automated refresh scheduled; documentation handed over. | [YYYY-MM-DD] |

* **Contingency Buffer:** `[X] business days` allocated to handle unanticipated schema errors, API downtime, or data pipeline bugs.

---

## 6. COMMUNICATION PLAN

To protect solo execution time while maintaining complete transparency with stakeholders, the following structured communication cadence will be maintained:

| Channel / Meeting Type | Cadence | Primary Audience | Objective |
| --- | --- | --- | --- |
| **Milestone Gate Reviews** | Phase Checkpoints | Approvers | Formal sign-off on deliverables, scope changes, and project transitions. |
| **Async Status Update** | Weekly (Friday Email/Slack) | All Stakeholders | Bulleted progress summary, completed tasks, upcoming goals, and active blockers. |
| **Technical Ad-Hoc Sync** | As Needed | Contributors | Technical problem-solving regarding databases, schemas, or server access. |

---

## 7. REFERENCES & TECHNICAL APPENDIX

* **Data Dictionary & Schema Notes:** `[Link to Data Description / Dictionary Documentation]`
* **Past Analytics & Related Work:** `[Link to prior related dashboard or query files]`
* **Stakeholder Context Documents:** `[Link to original business request or product roadmap]`

---
