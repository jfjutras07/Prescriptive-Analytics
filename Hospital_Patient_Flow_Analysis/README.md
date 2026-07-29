# Hospital Patient Flow Demand Analysis
### Integrated Healthcare Analytics, Workforce Optimization & Strategic Decision Support
**Advanced Modeling of Patient Demand, Time Series Forecasting, Nursing Allocation, Uncertainty Analysis & MCDA**

---

The objective of this project is to demonstrate how healthcare operational analytics, time series forecasting, operations research, and decision analysis methods can support strategic nursing workforce planning decisions.

The project develops an integrated analytical framework combining:

- Patient Flow Analytics: Analysis of historical hospital demand patterns, operational indicators, and patient volume dynamics.
- Time Series Forecasting: Modeling of future patient demand patterns, forecasting readiness assessment, and uncertainty evaluation to support workforce planning assumptions.
- Workforce Capacity Modeling: Representation of nursing availability, staffing requirements, workforce costs, and outsourced labor alternatives.
- Mathematical Optimization: Mixed Integer Linear Programming (MILP) to identify cost-effective nursing workforce allocation strategies under operational and financial constraints.
- Uncertainty Analysis: Monte Carlo simulation and sensitivity analysis to evaluate workforce planning robustness under demand and cost variability.
- Multi-Criteria Decision Analysis (MCDA): Strategic evaluation of workforce scenarios using stakeholder preferences, AHP-based criteria weighting, and TOPSIS-based scenario ranking.

By combining descriptive analytics, predictive modeling, prescriptive optimization, and strategic decision analysis, the framework transforms hospital operational data into an end-to-end decision-support system for workforce investment planning.

---

# Data Architecture & Preprocessing

The project uses healthcare operational datasets containing patient demand, forecasting outputs, workforce structure, scheduling information, and workforce costs.

## Integrated Data Components

**Patient Demand Data**

- Historical daily and hourly patient volumes
- Demand variability assessment
- Temporal patterns supporting workforce planning assumptions

**Forecasting Data**

- Time series demand modeling outputs
- Forecast performance indicators
- Future demand projections and uncertainty assessment

**Workforce Data**

- Department-level nursing availability
- Workforce schedules
- Internal labor costs
- Outsourced nursing cost assumptions

## Data Preparation

- Dataset validation and structural inspection
- Operational table extraction
- Workforce data transformation into optimization-ready inputs
- Engineering of department-level staffing assumptions
- Creation of decision variables and optimization constraints

---

# Notebook 1 – Hospital Operational Data Analysis

## Objective

Understand hospital operational characteristics and identify relevant indicators influencing patient flow and workforce requirements.

## Methods

- Exploratory data analysis
- Dataset profiling
- Operational indicator assessment
- Patient flow characterization

## Key Contribution

Provides the analytical foundation required to understand hospital activity patterns before forecasting and workforce optimization.

---

# Notebook 2 – Patient Demand Forecasting

## Objective

Develop forecasting models to evaluate future patient demand patterns and assess forecasting readiness.

## Methods

- Time series preparation
- Demand trend analysis
- Forecast validation
- Forecast performance evaluation
- Forecast uncertainty assessment

## Key Contribution

Provides predictive insights required to anticipate future operational demand and support workforce planning assumptions.

---

# Notebook 3 – Patient Flow Demand Analysis

## Objective

Analyze temporal demand behavior and validate the characteristics of hospital patient flow before applying workforce optimization methods.

## Methods

- Time series statistical analysis
- Demand frequency validation
- Missing value assessment
- Stationarity analysis
- Autocorrelation evaluation
- Temporal pattern exploration

## Key Findings

- Historical demand series showed stable operational behavior
- No major structural issues were identified in the analyzed demand patterns
- Demand characteristics supported the use of forecasting outputs as workforce planning inputs

## Decision Support Contribution

The notebook establishes the relationship between patient demand dynamics and workforce capacity requirements, ensuring that optimization decisions are based on validated operational patterns.

---

# Notebook 4 – Nursing Workforce Planning Optimization

## Workforce Optimization Model

A Mixed Integer Linear Programming (MILP) model is developed to determine the optimal allocation of additional nurses across hospital departments.

The model considers:

- Current nursing workforce availability
- Department-level staffing requirements
- Internal nurse hiring costs
- Outsourced nursing labor alternatives
- Annual workforce budget constraints

## Optimization Objective

Maximize workforce cost savings by replacing outsourced nursing capacity with internal hiring while maintaining minimum operational coverage requirements.

---

## Baseline Optimization Results

The optimization model identifies the most cost-effective workforce allocation strategy.

**Results:**

- Optimal allocation of **9 additional nurses**
- Annual workforce cost savings of **$572,000**
- All staffing constraints satisfied
- Workforce expansion concentrated in departments where internal hiring provides the highest economic value

## Key Insight

The optimization demonstrates that workforce investment decisions should prioritize departments where additional internal capacity generates the highest operational and financial benefits.

---

# Uncertainty & Sensitivity Analysis

## Monte Carlo Demand Simulation

A Monte Carlo simulation evaluates patient demand uncertainty using historical demand variability.

**Simulation Framework:**

- 10,000 simulated demand scenarios
- Historical demand distribution parameters
- Evaluation of operational uncertainty

**Findings:**

- Daily patient demand presents moderate variability around historical averages
- Demand uncertainty represents an important factor for workforce resilience
- Simulation results provide a foundation for future stochastic optimization approaches

---

## Budget Sensitivity Analysis

Multiple budget scenarios are evaluated to measure the impact of financial capacity on workforce decisions.

**Scenarios:**

- $750K
- $1M
- $1.25M
- $1.5M

**Key Insights:**

- Higher workforce budgets enable additional internal hiring
- Increased investment generates additional workforce savings
- Budget availability directly influences achievable operational improvements

---

## Nursing Coverage Sensitivity Analysis

The model evaluates different minimum staffing coverage assumptions.

**Scenarios:**

- 70% coverage
- 75% coverage
- 80% coverage

**Key Insight:**

Higher coverage requirements increase operational constraints and reduce optimization flexibility by limiting purely cost-driven workforce allocation.

---

## Outsourced Labor Cost Sensitivity Analysis

The impact of external nursing labor cost variations is evaluated.

**Scenarios:**

- -20% outsourced labor cost
- Baseline outsourced labor cost
- +20% outsourced labor cost

**Key Insight:**

External labor cost changes primarily affect the financial value of internal hiring while maintaining the same optimal workforce allocation under the defined constraints.

---

# Notebook 5 – Multi-Criteria Decision Analysis for Strategic Workforce Planning

## Decision Context

Optimization identifies mathematically efficient workforce solutions, but healthcare decisions require consideration of broader strategic priorities.

The MCDA framework evaluates workforce alternatives according to:

- Financial Efficiency
- Patient Coverage
- Operational Robustness
- Implementation Feasibility
- Workforce Sustainability

---

# Stakeholder-Based Criteria Weighting

A stakeholder workshop is simulated using six hospital profiles:

- Nursing Manager
- Clinical Coordinator
- Hospital Operations Manager
- Finance Representative
- Human Resources Representative
- Quality and Patient Safety Representative

Stakeholder preferences are aggregated using the **Analytic Hierarchy Process (AHP)**.

---

# AHP Criteria Weighting

Pairwise comparisons are performed using the Saaty fundamental scale.

The aggregated stakeholder judgments generate the following criteria weights:

| Criterion | Weight |
|---|---:|
| Patient Coverage | 0.34 |
| Operational Robustness | 0.24 |
| Workforce Sustainability | 0.18 |
| Financial Efficiency | 0.16 |
| Implementation Feasibility | 0.08 |

## Interpretation

Stakeholders prioritize patient coverage and operational resilience over purely financial optimization.

---

# AHP Consistency Assessment

The aggregated comparison matrix is evaluated using the Consistency Ratio (CR).

**Result:**

- Consistency Ratio: approximately 0.07

**Interpretation:**

The stakeholder judgments demonstrate acceptable consistency, confirming that the resulting criteria weights are sufficiently reliable for subsequent MCDA evaluation.

---

# TOPSIS Strategic Scenario Evaluation

*(Section under development)*

The final stage applies TOPSIS to rank workforce planning alternatives according to stakeholder-defined priorities.

Scenarios will be evaluated using:

- Financial performance
- Patient coverage
- Operational robustness
- Implementation feasibility
- Workforce sustainability

---

# Strategic Insights

## Workforce Planning Trade-offs

**Efficiency vs Operational Resilience**

- Cost-minimizing solutions may not always represent the most strategically desirable workforce strategy.
- Healthcare organizations must balance financial efficiency with patient safety and operational continuity.

## Optimization + MCDA Integration

- MILP identifies mathematically efficient and feasible workforce allocations.
- MCDA incorporates organizational preferences and strategic priorities.

Together, these methods provide a more complete decision-support framework.

---

# Actionable Recommendations

- Integrate forecasting outputs directly into future workforce optimization models.
- Combine mathematical optimization with stakeholder-based decision frameworks.
- Incorporate patient acuity, regulatory requirements, and clinical workload indicators in future models.
- Develop stochastic optimization approaches linking demand uncertainty with workforce decisions.
- Complete MCDA scenario ranking using TOPSIS methodology.

---

# Project Structure

## Notebook 1 – Hospital Operational Data Analysis

- Dataset exploration
- Patient flow analysis
- Operational indicator assessment

## Notebook 2 – Patient Demand Forecasting

- Time series preparation
- Forecasting models
- Forecast validation
- Demand uncertainty evaluation

## Notebook 3 – Patient Flow Demand Analysis

- Demand pattern analysis
- Time series validation
- Stationarity and autocorrelation analysis
- Operational demand characterization

## Notebook 4 – Nursing Workforce Planning Optimization

- Workforce capacity modeling
- MILP optimization
- Cost-saving workforce allocation
- Monte Carlo uncertainty analysis
- Sensitivity analysis

## Notebook 5 – Multi-Criteria Decision Analysis

- Stakeholder criteria definition
- AHP weighting methodology
- Consistency assessment
- TOPSIS scenario ranking *(in progress)*

---

# Key Takeaways

## Operational Analytics

Transforms hospital demand information into structured workforce planning inputs.

## Predictive Analytics

Time series forecasting provides insights into future patient demand and operational uncertainty.

## Optimization

Identifies cost-effective nursing allocation strategies under workforce and budget constraints.

## Risk Assessment

Evaluates how uncertainty and assumptions influence workforce decisions.

## Strategic Decision Support

Combines optimization results with stakeholder preferences to support complex healthcare planning decisions.

---

# Conclusion

This project demonstrates how healthcare workforce planning can evolve from descriptive analytics toward predictive, prescriptive, and strategic decision-making.

By integrating patient flow analysis, time series forecasting, mathematical optimization, uncertainty modeling, and multi-criteria decision analysis, the framework provides a transparent and explainable approach to workforce investment planning.

The combination of data analytics, operations research, and stakeholder-driven evaluation creates a robust foundation for future healthcare resource allocation applications.
