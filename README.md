# ⚙️ Operational Analytics: Automation Impact & Cycle-Time Risk Routing

End-to-end operations analytics project showing how workflow automation changes system behavior, and how risk-based routing can reduce service-target misses.

---

## Results at a glance
- Built a systems analysis of congestion dynamics (workload, utilization, variability, cycle time).
- Developed an operations dashboard to track throughput, cycle time, and manual-work reduction across implementation phases.
- Trained a risk model to identify high-risk long-cycle work (P90) and route top-risk items to priority handling.
- Used instrument-held-out GroupKFold evaluation to reduce leakage risk in operations data.

---

## What this project demonstrates
- **Systems thinking:** Causal feedback loops linking demand, capacity, variability, and delay.
- **Operational measurement:** Phase-aware KPIs showing stability vs. volatility over time.
- **Predictive decision support:** Risk-based queue routing to proactively reduce late work.

---

## Project artifacts

### 1) Systems framing (brief)
A concise systems analysis explaining why cycle time destabilizes under congestion and how automation changes the operating regime.

- [Systems Analysis Brief](Workflow_automation_systems_analysis.pdf)  
- Preview: causal network  
  ![Causal network](assets/causal-network.png)

### 2) Operational measurement (Tableau)
Interactive dashboard covering:
- throughput and cycle-time trends
- utilization signals
- manual-work reduction
- outcome stability by implementation phase

- [Interactive Dashboard](https://public.tableau.com/views/AutomationImpact-QCLabOperations/AutomationImpact?:language=en-US&:display_count=n&:origin=viz_share_link)

**Executive overview**  
![Executive Overview](assets/exec-overview.png)

**Implementation operations**  
![Implementation Operations](assets/implementation-operations.png)

**Operations view**  
![Operations](assets/lab-operations.png)

### 3) Predictive modeling notebook (priority routing)
Model identifies high-risk long-cycle items and simulates a priority routing policy.

- Target: **high-risk long cycle time (P90)**  
- Validation: **instrument-held-out GroupKFold**  
- Decision lens: service-target threshold + late-rate lift in routed queue  
- [Notebook: Ops ML routing model](ops-ml_sla-routing.ipynb)

![ROC + service target view](assets/ops-ml-visuals.png)

---
## Dataset Design

Because real laboratory operations data is typically proprietary, this project uses a synthetic dataset designed to represent common workflow patterns in regulated lab environments.

The simulation includes instrument type, test type, operator, product family, manual-entry status, automation phase, downtime flags, run duration, and turnaround time.

The dataset is not intended to estimate real-world ROI. It is used to demonstrate how operational data can be structured, monitored, and modeled to prioritize time-consuming work.

## Reproducibility

This project can be run locally using the provided conda environment.

```bash
# 1. Create environment
conda env create -f environment.yml

# 2. Activate environment
conda activate ops-ml

# 3. Launch Jupyter
jupyter notebook
```

Open:

```text
ops-ml_sla-routing.ipynb
```

Then:

- Select the `ops-ml` kernel  
- Run all cells (`Kernel → Restart & Run All`)

The notebook uses the dataset:

```text
data/qc_instrument_usage.csv
```

> Note: All file paths are relative to the repository root.

---

## Limitations & next steps
- Simulated data limits direct real-world generalization.
- Next: add calibration, temporal validation, and demand-shift policy tests.
- Extension: compare top-risk-only vs. capacity-aware routing.
