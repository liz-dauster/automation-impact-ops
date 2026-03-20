# Operational Analytics: Automation Impact and Cycle Time Risk Routing

Operations analytics project using systems analysis and modeling to improve workflow efficiency, cycle time, and SLA performance.

---

## What this project shows

- **Systems thinking:** feedback loops linking workload, variability, utilization, and cycle time
- **Operational measurement:** dashboards that quantify process changes over time
- **Predictive modeling for operations:** a model that identifies high-risk work and prioritizes it to reduce service-target misses

---

## Artifacts

### 1) Systems framing (brief)
A short systems analysis that explains why cycle time becomes unstable under congestion and how automation shifts regime behavior.

- [Systems Analysis Brief](Workflow_automation_systems_analysis.pdf)

<details>
  <summary><b>Preview: causal network</b></summary>

  ![Causal network](assets/causal-network.png)

</details>

---

### 2) Operational measurement (Tableau)
Interactive dashboard evaluating:
- throughput and cycle time trends
- utilization signals
- manual work reduction
- stability of outcomes across phases

- [Interactive Dashboard](https://public.tableau.com/views/AutomationImpact-QCLabOperations/AutomationImpact?:language=en-US&:display_count=n&:origin=viz_share_link)

<details>
  <summary><b>Dashboard previews</b></summary>

  **Executive overview**  
  ![Executive Overview](assets/exec-overview.png)

  **Implementation operations**  
  ![Implementation Operations](assets/implementation-operations.png)

  **Operations view**  
  ![Operations](assets/lab-operations.png)

</details>

---

### 3) Predictive modeling for operations notebook (priority queue routing)
Identifies the top 10% highest-risk work and prioritizes it to a priority queue to reduce service-target misses.
- Target: identifying **high-risk long cycle time** (P90)
- Validation: **instrument-held-out cross-validation** (GroupKFold)
- Stakeholder view: derived service-target threshold + **late-rate lift** in the routed queue

- [Notebook: Ops ML routing model](/ops-ml_sla-routing.ipynb)

<details>
  <summary><b>Notebook visuals</b></summary>

  ![ROC + service target view](assets/ops-ml-visuals.png)

</details>

---

## Data

Simulated dataset stored in:
- `data/qc_instrument_usage.csv`

---

## Run locally (conda)

```bash
conda env create -f environment.yml
conda activate ops-ml
jupyter notebook
