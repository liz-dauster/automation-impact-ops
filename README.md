# Automation Impact - QC Lab Operations

Systems + modeling case study evaluating workflow automation in a regulated QC lab  
using simulated operational data.

Connects strategy → measurement → modeling  
to test structural workflow stability under rising demand.

---

## Core Insight

Automation increases throughput and reduces cycle time.

Downtime risk is structural.
It concentrates under nonlinear, high-complexity, high-utilization regimes, 
not simply higher volume.

---

## Project Components

### 1. Systems Framing

Operational uncertainty analysis:

- Workload–variability–utilization feedback
- Capacity saturation risk
- Compliance vs performance trade-offs
- Manual friction → instability pathways

[Systems Analysis Brief](QC_Workflow_Automation_Systems_Analysis.pdf)

---

### 2. Operational Measurement

Tableau dashboard evaluating:

- Throughput (runs / instrument-hour)
- Cycle time
- Instrument utilization
- Manual entry reduction
- Failure rate stability

[Interactive Dashboard](https://public.tableau.com/views/AutomationImpact-QCLabOperations/AutomationImpact?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

### 3. Downtime Risk Modeling

Instrument-day nonlinear regime detection.

- Leakage-aware aggregation
- Linear baseline (ROC-AUC ~ 0.48)
- Threshold detection via shallow decision tree
- Identification of structural instability drivers

[Modeling Notebook](instrument_downtime_risk_modeling.ipynb)

---

## Data

Simulated datasets included in `/data` for reproducibility.

---

## Dashboard Preview

Executive Overview  
![Executive Overview](assets/exec-overview.png)

Implementation Operations  
![Implementation Operations](assets/implementation-operations.png)

Lab Operations  
![Lab Operations](assets/lab-operations.png)
