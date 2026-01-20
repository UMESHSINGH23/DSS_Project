# Decision Support System for Distribution Center Optimization (Germany)

## Project Overview
This project develops a **Decision Support System (DSS)** to support strategic decision-making for the **optimal placement of regional distribution centers (DCs)** for a retail company operating in **Germany**.

The system integrates:
- Multi-source retail and logistics data
- Optimization-based decision modeling
- Scenario and sensitivity analysis
- Optional machine learning–based demand forecasting
- Visual presentation using figures, tables, and optional dashboards

The primary objective is to **minimize total logistics cost while maintaining service performance** under different demand and operational scenarios.

---

## Problem Statement
Retail companies face increasing logistics complexity due to:
- Regional demand variability
- Rising transportation and fuel costs
- Service-level expectations
- Warehouse capacity constraints

This DSS helps answer:
> *Which distribution centers should be opened, and how do demand and cost changes affect this decision?*

---

## DSS Architecture

| Layer | Description |
|-----|-------------|
| **Data Layer** | Retail sales, logistics, and warehouse datasets (CSV/Excel) |
| **Model Layer** | Optimization (Linear Programming) + Scenario Analysis |
| **Decision Layer** | Distribution center selection and regional assignment |
| **Presentation Layer** | Python-generated figures, tables, and optional dashboards |

---

## Repository Structure

DSS_Project/
│
├── app.py                         # Optional Streamlit interface
├── final_dss_decision_dataset.csv # Integrated DSS dataset
│
├── RQ_data/                       # Research Question outputs
│   ├── region_demand.csv
│   ├── cost_comparison.csv
│   ├── service_distribution.csv
│   ├── technique_comparison.csv
│   └── demand_scenario_costs.csv
│
├── RQ_figures/                    # All DSS figures (PNG)
│
├── TABLE/                         # DSS tables (CSV)
│
├── requirements.txt               # Streamlit dependencies
└── README.md                      # Project documentation

---

## Research Questions & Answers

---

### **RQ1: What geographic and demand factors influence optimal DC placement in Germany?**

**Answer:**  
Regional demand concentration is the primary factor influencing distribution center placement. Regions with consistently higher aggregated demand exert greater influence on DC location decisions because proximity reduces transportation cost and improves service reliability. Demand patterns act as a proxy for population density and market size.

**Evidence:**  
- `RQ_data/region_demand.csv`
- Figure: *Regional Demand Distribution*

---

### **RQ2: How does the DSS minimize total logistics cost?**

**Answer:**  
The DSS uses a **linear programming–based optimization model** to evaluate multiple DC configuration scenarios. By balancing transportation costs, facility costs, and service coverage, the system identifies the number of distribution centers that minimizes total logistics cost without over-provisioning infrastructure.

**Evidence:**  
- `RQ_data/cost_comparison.csv`
- Figure: *Cost vs Number of Distribution Centers*

---

### **RQ3: Which decision support techniques are most effective for DC location problems?**

**Answer:**  
Linear Programming was identified as the most effective technique due to its:
- High accuracy
- Low computational complexity
- Transparency and interpretability

While clustering and genetic algorithms are useful for exploratory analysis, optimization-based methods are more suitable for strategic decision-making.

**Evidence:**  
- `RQ_data/technique_comparison.csv`
- Table: *Comparison of DSS Techniques*

---

### **RQ4: How does demand forecasting improve DC decision accuracy?**

**Answer:**  
Incorporating projected demand scenarios significantly improves decision robustness. Scenario analysis demonstrates that increasing demand leads to higher logistics costs and may require additional distribution capacity or alternative DC placement strategies.

This validates the importance of demand forecasting within a DSS framework.

**Evidence:**  
- `RQ_data/demand_scenario_costs.csv`
- Figure: *Impact of Demand Growth on Cost*

---

### **RQ5: What is the impact of DC location scenarios on service performance?**

**Answer:**  
Service performance improves when regional demand is evenly distributed across selected DCs. Scenarios with balanced regional assignments reduce delivery risk and improve fulfillment reliability, whereas under-provisioned scenarios increase service pressure.

**Evidence:**  
- `RQ_data/service_distribution.csv`
- Figure: *Service Coverage by Distribution Center*

---

## Key DSS Outputs

- Optimal number of distribution centers
- Estimated total logistics cost
- Regional demand coverage
- Scenario-based cost sensitivity
- Managerial insights for strategic planning

---

## Optional Enhancements
- **Machine Learning** for demand forecasting (used for scenario generation)
- **Streamlit dashboard** for interactive what-if analysis (optional UI layer)
- **Power BI** or report-based visualization for executive presentation

---

## Tools & Technologies

- Python (Pandas, Matplotlib, Scikit-learn)
- Linear Programming (PuLP / optimization logic)
- Google Colab (analysis & modeling)
- GitHub (version control)
- Streamlit (optional interface)

---

## Academic Note
This project focuses on **decision logic and interpretability**, aligning with MSc-level expectations for Decision Support Systems. Visualization tools are used only to enhance decision understanding and do not replace analytical modeling.

---
GROUP 3
58326751	Umesh	Singh
57844260	Inamulhasan	Syed
80443189	Talatcan	Gültekin
62472203	Cisem Bayer	Ferah
65589515	Anandhu	Rajappan Krishnan 
MSc Data Science  
Decision Support Systems Project  

---

##  Conclusion
This project demonstrates a complete and robust **Decision Support System** capable of supporting strategic distribution planning decisions under uncertainty. The system integrates data, models, scenarios, and insights in a structured and academically sound manner.

---
