# Strategic Portfolio & Operations Optimization  
### Integrated Decision-Making & Risk-Resilient Planning  
**Advanced Modeling of Project Portfolios, Resource Capacity & Operational Resilience**

---

The goal of this project is to optimize a multi-year organizational portfolio using **project-level financial, operational, and strategic data**, incorporating:

- Multi-year **budget forecasts** and human resource capacities (2026–2028)  
- Project-specific **strategic impacts**: Asset, Legal, Financial, Internal, Adaptation  
- **Operational constraints**: Resource saturation, execution risk, prerequisites  
- **Scenario modeling**: Baseline, capacity boost, dynamic phasing  
- **Stochastic simulation**: Monte Carlo assessment of delivery risk and portfolio robustness  

By combining deterministic optimization with risk-aware simulations, the model enables **actionable insights for project selection, phasing, and contingency planning**.

---

### Data Architecture & Preprocessing

**Consistency & Capacity Alignment**  
- Integrated **3 master tables**: Projects, Resources, and Capacity per role/year.  
- Cleared column and value inconsistencies; replaced missing resource allocations with zeros.  
- Normalized project ROI and strategic impacts via **Robust Scaling** to mitigate outlier bias.  

**Strategic Bucketing**  
- Projects grouped into 4 strategic types:  
  - **Asset Management (Type 1)**  
  - **Service Development (Type 2)**  
  - **Growth & Expansion (Type 3)**  
  - **Continuous Improvement (Type 4)**  
- Allocation targets with ±5% tolerance ensure balance across high-value and critical initiatives.  

---

### Optimization & Portfolio Modeling

**Baseline Optimization**  
- LP-based selection under budget ($1M), 90% resource utilization, and risk constraints.  
- Resulted in **18 selected projects**, primarily reinforcing internal optimization and asset stability.  

**Capacity Boost Scenario**  
- Simulated **+10% human resource availability**, marginally increasing projects from 18 → 19.  
- Revealed that **resource saturation was not the main bottleneck**; strategic phasing offers more leverage.  

**Dynamic Phasing**  
- Shifted start dates across 2026–2028 to smooth peaks in capacity demand.  
- Expanded portfolio to **25 projects**, including backloaded initiatives.  
- Enabled more balanced execution without increasing payroll costs, though average ROI turned slightly negative, reflecting strategic rather than purely financial prioritization.

---

### Risk Assessment & Contingency Planning

**Portfolio-Level Risk Metrics**  
- **Budget Risk Index**: Weighted exposure of high-cost, high-risk projects.

<img width="1187" height="686" alt="image" src="https://github.com/user-attachments/assets/061a3885-2dd9-48f0-9fbd-02ddffbd4d14" />

- **HR Complexity Index**: Multiplicative risk from resource demands and dependency chains.  
- **Dynamic Contingency Fund**: $174k (~16.4% of total portfolio) to cover top 10% risk projects.  

**Red Flag Projects**  
- High financial exposure: Projects [26, 28]  
- High HR complexity: Projects [19, 27]  

**Monte Carlo Simulation**  
- 10,000 simulations assessing portfolio failure probability.  
- ~14–15 projects expected delivered out of 18, with ~15% chance of total portfolio failure.  
- Risk concentrated on a few critical projects (31, 28, 17), guiding executive monitoring priorities.

---

### Strategic Insights

**Portfolio Posture & Trade-offs**  
- “Stability-first with selective growth”: preserves core operations while cautiously expanding high-value initiatives.  
- Soft strategic bucketing and dynamic phasing improve resilience and execution feasibility.  
- Scenario analysis confirms **budget sensitivity** > human resource sensitivity, highlighting capital allocation as the key constraint.  

**Actionable Recommendations**  
- Maintain contingency reserves aligned with identified red-flag projects.  
- Use phasing and timing adjustments rather than increasing headcount where possible.  
- Prioritize continuous improvement and asset management projects to safeguard long-term capability.  

---

### Project Structure

- **Notebook 1 – Strategic Foundations & Organizational Digital Twin**  

  Introduces **PARO (Projects, Assets, Risks, and Operations)**, a multi-layered Decision Support System (DSS) that simulates a cohesive corporate ecosystem.  
  Focuses on:  
    - Strategic portfolio optimization under budget and resource constraints  
    - Linking long-term organizational strategy with operational execution  
    - Establishing the foundation for prescriptive modules in Projects, Assets, and Risks  

- **Notebook 2 – Portfolio Optimization & Dynamic Phasing**  

  Implements operational-level optimization and scenario analysis:  
    - Baseline portfolio selection under strategic bucket constraints  
    - Resource capacity simulations (e.g., staffing boosts)  
    - Dynamic project phasing to level workloads over multiple years  
    - Financial and HR risk scoring, contingency fund calculation  
    - Monte Carlo simulations to assess portfolio robustness and delivery risk
---

### Key Takeaways

- **Operational Bottlenecks Defined**: Key roles exceeding 90% capacity create real execution ceilings.  
- **Strategic Phasing Unlocks Value**: Temporal redistribution enables more projects without increasing headcount.  
- **Risk-Aware Portfolio**: Contingency fund covers high-exposure projects, maintaining execution capability.  
- **Balanced Strategic Posture**: Portfolio favors resilience and capability-building over immediate ROI maximization.

---

### Limitations & Considerations

- Static resource assumptions may need recalibration for future planning cycles.  
- ROI can turn negative when projects are prioritized for strategic rather than financial objectives.  
- High-risk projects require **active monitoring and executive intervention** to avoid overrun.

---

### Conclusion

This project demonstrates how **data-driven portfolio optimization** can integrate financial, operational, and strategic dimensions to support **robust, explainable, and actionable decision-making**, ensuring that organizational initiatives are both **feasible and resilient**.
