## Automation Impact - QC Lab Operations

This project is an applied data science case study evaluating the operational impact of integrating QC lab instruments with automation software using simulated laboratory data.

The analysis spans executive, implementation, and lab operations perspectives, examining throughput, utilization, available capacity, and analyst workflow changes under operational constraints.

🔗 **Tableau Story (interactive):** <https://public.tableau.com/views/AutomationImpact-QCLabOperations/AutomationImpact?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link>

### Key questions
- Did automation improve throughput and cycle time?
- How did instrument utilization and available capacity shift?
- How was analyst effort reallocated following system go-live?

### Analytical approach
- Use **runs per instrument-hour** as sample throughput
- Measure instrument utilization and available capacity
- Assess analyst workflow via manual vs automated runs
- Robust statistics (median, IQR) used for skewed operational data

### Data
The dataset is simulated and included in the `data/` directory to support reproducibility.

### Dashboards

#### Executive Overview
![Executive Overview](images/exec-overview.png)

#### Implementation Operations
![Implementation Operations](images/implementation-operations.png)

#### Lab Operations
![Lab Operations](images/lab-operations.png)
