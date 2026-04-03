# Food Distribution Optimization
### Integrated Humanitarian Decision-Making & Risk-Resilient Allocation
**Advanced Modeling of Food Insecurity Phases, Resource Constraints & Operational Impact**

---

The objective of this project is to optimize global humanitarian resource allocation using food insecurity data (IPC/Cadre Harmonisé) and operations research models. It integrates:

- Population Distribution by Phase: Granular analysis of severity levels (Phases 1 to 5).
- Humanitarian Impact Proxies: Public health outcomes, economic burden, and risk of deterioration.
- Operational Constraints: Limited budgets, mandatory minimum presence, and capacity ceilings.
- Scenario Modeling: Strategy-based approaches (Urgency/Severity, Efficiency/Human ROI, Preventive/Resilience).
- Stochastic Simulation: Monte Carlo assessment of allocation robustness under data uncertainty.

By combining deterministic optimization with risk-aware simulations, the model generates actionable insights for geographic prioritization and strategic intervention planning.

---

### Data Architecture & Preprocessing

- Multi-Country Integration: Consolidated data from 52 countries, aligned to a common time window (Oct–Dec 2025).
- Data Validation: Cross-check between total population and phase distributions; exclusion of inconsistent datasets (e.g., Niger) to ensure solver reliability.
- Normalization: MinMax scaling to prevent bias between high-population countries (NGA) and high-intensity contexts (PSE).

**Feature Engineering**

- Severity Computation: Hybrid Priority Score combining:
  - Relative severity (% of population in Phase 3+)
  - Absolute scale (number of affected individuals)
- Weighted Cost Structure:
  - Intervention cost indexed to severity
  - Phase 5 estimated at ~5× the cost of Phase 3

---

### Optimization & Allocation Modeling

**Baseline Optimization**

- Linear Programming model maximizing impact-per-dollar under a $1M budget constraint.

**Results:**
- Resource concentration on efficiency hubs (NGA, CMR, GHA)
- Maintenance of a minimum allocation across ~15 countries to ensure baseline coverage

---

### Sensitivity Analysis (Budget Scaling)

- Simulation across budget scenarios ($0.5M → $5M)

**Key Insight:**
- Progressive “entry sequence” of countries into the allocation portfolio
- Identification of “swing zones” receiving funding only after core countries reach saturation

<img width="1061" height="529" alt="image" src="https://github.com/user-attachments/assets/18bf2909-9252-452c-9054-889d7385d079" />

---

### Monte Carlo Simulation

- 500 iterations

**Findings:**

- Structural Pillars:
  - Nigeria (NGA) and Cameroon (CMR) hit funding caps in ~100% of simulations

- Volatility Zones:
  - Chad (TCD) and Ghana (GHA) show high sensitivity to data uncertainty
  - Act as strategic arbitrage zones depending on data accuracy

---

### Strategic Trade-offs (Scenario Modeling)

- **Urgency-First Strategy**
  - Prioritizes Phases 4–5 regardless of cost
  - Strong allocation to high-severity contexts (e.g., PSE)

- **Efficiency Strategy**
  - Maximizes total beneficiaries reached
  - Favors lower-cost, high-impact countries (GHA, CMR)

- **Preventive Strategy**
  - Targets fragile contexts at risk of deterioration
  - Focuses on medium-severity, high-volatility countries

---

### Risk Assessment & Robustness

**Global Risk Metrics**

- Cost-Efficiency Gap:
  - Difference between theoretical impact and operational reality

- Coverage Ratio:
  - Share of critical population effectively reached

<img width="966" height="692" alt="image" src="https://github.com/user-attachments/assets/2a4d33c0-1c6a-4023-bfa6-e71ce5faa3c3" />

---

### Strategic Insights

**Humanitarian Trade-offs**

- “Efficiency vs Equity”:
  - Maximizing total beneficiaries tends to deprioritize high-cost conflict zones
  - Requires explicit policy decisions to rebalance allocation

- Anchor Countries:
  - NGA and CMR act as structural hubs in the allocation portfolio

---

### Actionable Recommendations

- Implement redistribution mechanisms to avoid “forgotten crises” in minimum-funded countries
- Strengthen data collection in volatility zones identified by Monte Carlo simulations
- Define a clear allocation doctrine (Efficiency vs Urgency vs Prevention) prior to budget cycles

---

### Project Structure

**Notebook 1 – Data Preparation & Exploratory Analysis**
- IPC data cleaning and validation
- Phase distribution analysis

**Notebook 2 – Optimization Modeling & Prescriptive Analytics**
- Hybrid Priority Score construction
- Linear Programming solver implementation
- Geospatial visualization of food insecurity
- Scenario analysis and Monte Carlo simulations
- Interactive allocation maps (Plotly Choropleth)

---

### Key Takeaways

- Identified Efficiency Gains:
  - Optimization reveals high-impact, cost-efficient allocation opportunities

- Scale of Unmet Needs:
  - Highlights the gap between available funding and required coverage

- Evidence-Based Decision-Making:
  - Transition from descriptive analytics to prescriptive optimization

---

### Conclusion

This project demonstrates how portfolio optimization techniques can be applied to humanitarian operations by integrating health, economic, and risk dimensions.

It provides a robust, transparent, and explainable framework to support decision-makers in allocating limited resources where they generate the highest human impact.
