## Automation Impact - QC Lab Operations

Applied systems analysis and data science case study evaluating workflow automation in a regulated QC laboratory using simulated operational data. 
This project connects strategy → measurement → modeling to assess structural workflow stability under rising demand.

🔎 Executive Summary:

Automation improves throughput and reduces cycle time, but operational stability depends on managing complexity, workload pressure, and capacity saturation risk.

The analysis shows:  
- Linear models do not explain downtime risk
- Downtime clusters under nonlinear, high-complexity regimes
- Structural workflow design, not volume alone, drives stability
  
<br>

### Project Components  
1️⃣ **Systems Analysis Brief**  
Structural framing of automation under operational uncertainty

Explores:  
- Workload–variability–utilization feedback loops
- Capacity saturation risk
- Compliance vs. performance trade-offs
- Causal pathways linking manual friction to instability

📄 [Read the Systems Analysis Brief](QC_Workflow_Automation_Systems_Analysis.pdf)

<br>

2️⃣ **Dashboard**  
Operational performance measurement

Evaluates:
- Throughput (runs per instrument-hour)
- Cycle time
- Instrument utilization
- Manual entry reduction
- Failure rate stability

🔗 [View the Interactive Tableau Dashboard](https://public.tableau.com/views/AutomationImpact-QCLabOperations/AutomationImpact?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

<br>

3️⃣ **Downtime Risk Modeling**  
Instrument-day nonlinear risk regimes

Demonstrates:
- Leakage-aware aggregation
- Linear model limitations (ROC-AUC ~0.48)
- Threshold-based regime detection via shallow decision tree
- Structural drivers of downtime risk

📓 [View the Modeling Notebook](instrument_downtime_risk_modeling.ipynb)

Data  
Simulated datasets included in /data for reproducibility.

<br>

### Tableau Dashboard Preview:

#### Executive Overview
![Executive Overview](assets/exec-overview.png)

#### Implementation Operations
![Implementation Operations](assets/implementation-operations.png)

#### Lab Operations
![Lab Operations](assets/lab-operations.png)
