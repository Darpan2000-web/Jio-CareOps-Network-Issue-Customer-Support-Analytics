# Jio CareOps – Network Issue & Customer Support Analytics

**A Python-based telecom analytics project focused on customer complaint investigation, network incident analysis, recharge failures, service request monitoring, and operational risk prioritization.**

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Status](https://img.shields.io/badge/Project-Completed-success)

## Project Overview

Customer support and network operations teams often need to investigate information scattered across multiple datasets. Identifying high-priority complaints becomes difficult when network incidents, recharge failures, customer details, and service requests are stored separately.

This project develops a reproducible Python-based analytics workflow to integrate these sources, clean and validate records, investigate individual complaints, and prioritize cases using transparent business rules.

The project simulates a telecom Customer Care and Network Operations environment.

**Important:** This is an educational project using fictional training data. It does not contain actual Jio operational or customer records and is not affiliated with or endorsed by Reliance Jio.

## Business Objectives

- Analyze customer complaint patterns and establish a complaint baseline.
- Clean and standardize inconsistent complaint records.
- Investigate network incidents at cell-site level.
- Identify recharge failures and potential refund risks.
- Monitor unresolved service requests and SLA follow-ups.
- Analyze customer complaints by city, circle, and repeated customer contacts.
- Build a complaint-level investigation dataset.
- Assign explainable P0–P3 operational priorities.
- Generate structured CSV and Excel reports for operational review.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data processing and analysis |
| Pandas | Data cleaning, transformation, and integration |
| NumPy | Numerical operations |
| Jupyter Notebook | Interactive analysis and documentation |
| JSON | Reference data processing |
| Excel / CSV | Data sources and report exports |

## Dataset Information

The project uses three primary input files:

| Dataset | Description |
|---|---|
| `complaints.csv` | Customer complaint records |
| `network_issue_reports.xlsx` | Network incident and cell-site reports |
| `careops_reference.json` | Customer, cell-site, recharge failure, service request, and operational reference information |

### Initial Dataset Overview

- Customer complaints: 5,000 records
- Network incident reports: 1,300 records
- Multiple reference collections are available in the JSON source.

All records are fictional and intended for learning and analytical practice.

## Project Workflow

The notebook is organized into ten milestones.

| Milestone | Analysis |
|---|---|
| 01 | Establish the complaint baseline |
| 02 | Load Excel network data and JSON reference collections |
| 03 | Validate and standardize complaint records |
| 04 | Prepare network incident signals |
| 05 | Audit recharge failures and refund risks |
| 06 | Detect service requests and SLA follow-ups |
| 07 | Analyze city, circle, and repeated customer impact |
| 08 | Build the complaint-level investigation view |
| 09 | Prioritize complaints using explainable business rules |
| 10 | Export operational reports and create a searchable case view |

## Data Integration & Quality Checks

A major focus of this project is maintaining data accuracy while combining multiple sources.

The workflow includes:

- Duplicate complaint identification and removal.
- Missing-value assessment.
- Standardization of complaint categories and statuses.
- Date and monetary field validation.
- Network incident aggregation at cell-site level.
- Recharge and service-request aggregation at complaint level.
- Preservation of unmatched records for investigation.
- Validation of complaint counts after data integration.

### Final Integrated Dataset

The final complaint-level investigation dataset contains:

- **4,901** unique complaint records.
- **57** columns after source integration.
- **0** duplicate complaint IDs.
- **0** missing customer IDs.
- **0** missing cell-site IDs.

The exported priority report contains 66 columns.

## Explainable Complaint Prioritization

The project uses a rule-based prioritization framework rather than an opaque machine learning model.

Four risk signals are evaluated:

1. Severe network incident or down/inactive/outage cell-site condition.
2. Recharge failure or refund-related risk.
3. Escalated or SLA-review service request.
4. Three or more complaints from the same customer.

### Priority Classification

| Priority | Risk Signals | Interpretation |
|---|---:|---|
| P0 | 3–4 | Highest priority |
| P1 | 2 | High priority |
| P2 | 1 | Medium priority |
| P3 | 0 | Lower priority |

### Final Priority Distribution

| Priority | Complaint Count |
|---|---:|
| P0 | 990 |
| P1 | 2,370 |
| P2 | 1,417 |
| P3 | 124 |
| **Total** | **4,901** |

These classifications are rule-based operational recommendations, not predictions of actual customer outcomes.

## Final Deliverables

The notebook generates two principal reports:

**1. `jio_complaint_priority_report.csv`**

A complaint-level investigation and prioritization report containing customer, network, recharge, service-request, and risk information.

**2. `jio_careops_operations_summary.xlsx`**

An Excel workbook containing operational summary information for further review.

The notebook also includes a searchable case-filtering workflow for investigating complaints by priority, city, circle, issue group, and complaint ID.

## Automated Assessment

The completed notebook includes an automated milestone self-assessment.

| Assessment | Result |
|---|---:|
| Completed milestones | 10 / 10 |
| Automated assessment score | 100 / 100 |
| Checks needing attention | 0 |

This is a formative notebook self-check. It validates selected output structures and business rules; it does not replace independent review of calculations and written findings.

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/Darpan2000-web/Jio-CareOps-Network-Issue-Customer-Support-Analytics.git
```

### 2. Open the project folder

```bash
cd Jio-CareOps-Network-Issue-Customer-Support-Analytics
```

### 3. Install dependencies

```bash
pip install pandas numpy openpyxl jupyter
```

### 4. Keep the input datasets available

Ensure the following files are accessible in the notebook's configured data directory:

```text
complaints.csv
network_issue_reports.xlsx
careops_reference.json
```

The notebook uses the current working directory outside Google Colab. If you store datasets in a separate folder, update `DATA_DIR` accordingly.

### 5. Run the notebook

```bash
jupyter notebook
```

Open `Jio_CareOps_Student_Starter.ipynb` and run all cells from beginning to end.

The notebook generates the final CSV and Excel reports after successful execution.

## Key Learning Outcomes

Through this project, I practiced:

- Real-world data cleaning and preprocessing.
- Multi-source data integration using Pandas.
- One-to-many relationship handling and aggregation.
- Data-quality validation and reconciliation.
- Complaint-level investigation.
- Rule-based risk scoring and prioritization.
- Operational reporting and structured data exports.
- Building reproducible analytical workflows.

## Author

**Darpan Banerjee**

M.Sc. Computer Science | Data Analytics

- GitHub: https://github.com/Darpan2000-web
- Portfolio: https://darpan2000-web.github.io/

---

*This project was developed for educational and portfolio purposes using fictional telecom training datasets.*
