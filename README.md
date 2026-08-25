# EcoShock

## A Graph-Based Economic Shock Propagation and Decision Support System

> **EcoShock** is an explainable, rule-based decision support system for analyzing how economic shocks propagate across interconnected sectors and affect different socioeconomic groups.

EcoShock represents an economy as a network of connected sectors and models how an initial disturbance—such as a war, pandemic, fuel disruption, recession, or supply shock—can propagate through the system.

Unlike a black-box prediction model, EcoShock focuses on **transparency and scenario-based reasoning**. Users can inspect sector relationships, modify shock severity, perform sensitivity analysis, and observe how changes propagate through the modeled economic system.

---

## Table of Contents

* [Motivation](#motivation)
* [Research Question](#research-question)
* [System Overview](#system-overview)
* [System Architecture](#system-architecture)
* [Economic Shock Propagation Model](#economic-shock-propagation-model)
* [Core Features](#core-features)
* [Economic Sectors](#economic-sectors)
* [Social Impact Analysis](#social-impact-analysis)
* [Sensitivity Analysis](#sensitivity-analysis)
* [Project Structure](#project-structure)
* [Technologies Used](#technologies-used)
* [Installation](#installation)
* [Usage](#usage)
* [Validation and Evaluation](#validation-and-evaluation)
* [Applications](#applications)
* [Limitations](#limitations)
* [Future Work](#future-work)
* [Research Relevance](#research-relevance)

---

# Motivation

Economic crises rarely affect only one sector. A disruption in one part of the economy can create a chain reaction:

```text id="98h8v7"
Global Shock
     │
     ▼
Energy / Commodity Prices
     │
     ▼
Transportation Costs
     │
     ▼
Food and Production Costs
     │
     ▼
Cost of Living
     │
     ▼
Impact on Different Social Groups
```

For example, an increase in oil prices may affect fuel prices, transportation, agricultural production, food prices, household expenditure, inflation, and different socioeconomic groups.

EcoShock addresses the question:

> **How can an initial economic shock propagate through an interconnected economic system, and which sectors and social groups may be most affected?**

---

# Research Question

> **Can an interpretable graph-based framework model the propagation of economic shocks across multiple sectors and provide scenario-based decision support without relying exclusively on black-box machine learning models?**

EcoShock combines:

1. Expert-defined economic relationships
2. A weighted directed graph
3. Rule-based scenario interpretation
4. Shock propagation
5. Sensitivity analysis
6. Sector-level impact assessment
7. Social-group impact analysis
8. Automated reporting

---

# System Overview

```text id="vwv4nb"
                ┌─────────────────────┐
                │  Crisis / Scenario  │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Scenario Processing │
                │ & Rule Matching     │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Initial Shock       │
                │ Identification      │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Graph Propagation   │
                │ Engine              │
                └──────────┬──────────┘
                           │
              ┌────────────┼────────────┐
              ▼            ▼            ▼
       ┌────────────┐ ┌──────────┐ ┌─────────────┐
       │ Sector     │ │ Economic │ │ Social      │
       │ Impacts    │ │ Effects  │ │ Impacts     │
       └─────┬──────┘ └──────────┘ └──────┬──────┘
             │                              │
             └──────────────┬───────────────┘
                            ▼
                 ┌─────────────────────┐
                 │ Sensitivity Analysis│
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Decision Support &  │
                 │ Automated Reporting │
                 └─────────────────────┘
```

---

# System Architecture

## Layer 1: Scenario Input

Users provide information about an economic event, such as:

* War or geopolitical conflict
* Pandemic
* Oil supply disruption
* Fuel crisis
* Economic recession
* Trade disruption
* Natural disaster
* Custom scenario

## Layer 2: Rule-Based Knowledge

This layer contains economic relationships and rules.

Example:

```text id="svwrtb"
IF oil supply decreases
THEN fuel price pressure increases

IF fuel prices increase
THEN transportation costs increase

IF transportation costs increase
THEN food distribution costs may increase
```

The objective is to provide an **interpretable mapping** from an initial crisis to potential downstream consequences.

## Layer 3: Graph Propagation Engine

The economy is modeled as:

[
G = (V, E)
]

where:

* (V) represents economic sectors or components.
* (E) represents directed relationships between them.

A weighted edge (w_{ij}) represents the relative strength of a transmission pathway from node (i) to node (j).

Conceptually, propagation can be represented as:

[
S_j^{(t+1)}
===========

f\left(
S_j^{(t)},
\sum_i w_{ij}S_i^{(t)}
\right)
]

where (S_j^{(t)}) is the impact score of sector (j), (w_{ij}) is a connection strength, and (f(\cdot)) represents the propagation mechanism defined by the project.

## Layer 4: Impact Analysis

The system summarizes potential effects across:

* economic sectors,
* consumer costs,
* market-related components,
* and socioeconomic groups.

Results are intended for **scenario exploration and decision analysis**, not deterministic forecasting.

## Layer 5: Sensitivity Analysis

Users can vary selected assumptions, including:

* Oil price increase
* Food supply disruption
* Unemployment
* Currency depreciation
* Interest-rate changes

## Layer 6: Reporting

The reporting module summarizes:

* scenario information,
* affected sectors,
* impact pathways,
* social-group assessments,
* sensitivity results,
* and key observations.

---

# Economic Shock Propagation Model

A typical transmission pathway is:

```text id="g6ttw1"
Oil Supply Disruption
        │
        ▼
Fuel Prices
        │
        ▼
Transportation Costs
        │
        ▼
Agriculture / Logistics
        │
        ▼
Food and Groceries
        │
        ▼
Cost of Living
        │
        ▼
Social Groups
```

The graph-based approach allows EcoShock to analyze **indirect consequences**, rather than only direct effects.

---

# Core Features

## 1. Crisis Impact Simulation

Predefined scenarios include:

* Russia–Ukraine War
* COVID-19 Pandemic
* Global Fuel Crisis
* Global Recession
* US–China Trade War

The framework can also be extended to additional scenarios.

## 2. Custom Scenario Analysis

Users can provide custom descriptions such as:

```text id="yiy3hz"
Major earthquake causing infrastructure disruption
```

or:

```text id="mirc9d"
Global oil supply disruption leading to higher fuel prices
```

The scenario engine uses the project's rule-based logic to identify relevant concepts and generate an initial shock configuration.

## 3. Graph-Based Shock Propagation

The propagation engine:

1. Identifies the initial shock.
2. Locates affected graph nodes.
3. Traverses connected sectors.
4. Applies defined propagation relationships.
5. Aggregates downstream effects.
6. Produces sector-level impact information.

## 4. Multi-Sector Analysis

The current framework includes:

* Fuel & Petroleum
* Healthcare
* Food & Groceries
* Gold
* Transport
* Agriculture
* Electronics
* Automobile
* Real Estate
* Stock Market
* Tourism

## 5. Social Impact Analysis

EcoShock examines potential differences across:

* Rich
* Upper Middle Class
* Lower Middle Class
* Poor

This provides a distributional perspective on how economic shocks may affect different groups.

## 6. Explainable Decision Support

EcoShock is designed to help answer:

* Which sectors are directly affected?
* Which sectors are affected indirectly?
* What pathways connect the initial crisis to downstream impacts?
* Which assumptions generate the largest changes?
* Which social groups are potentially most exposed?

---

# Sensitivity Analysis

Sensitivity analysis investigates how model outputs change when assumptions are varied.

For a parameter (x), the impact can be represented conceptually as:

[
I(x)
]

and compared over:

[
x \in {x_1, x_2, x_3, \ldots, x_n}
]

This can help identify:

* highly sensitive sectors,
* relatively stable sectors,
* important assumptions,
* and parameters with large downstream effects.

Because EcoShock is a rule- and graph-based system, sensitivity analysis is particularly important for understanding the dependence of results on model assumptions.

---

# Project Structure

```text id="76espt"
EcoShock/
│
├── app.py
├── requirements.txt
│
├── data/
├── reports/
├── assets/
│
├── modules/
│   ├── graph_engine.py
│   ├── scenario_engine.py
│   ├── sensitivity_analysis.py
│   └── report_generator.py
│
└── README.md
```

| Module                    | Purpose                                              |
| ------------------------- | ---------------------------------------------------- |
| `graph_engine.py`         | Builds and traverses the economic dependency graph   |
| `scenario_engine.py`      | Processes predefined and custom scenarios            |
| `sensitivity_analysis.py` | Evaluates the effect of changing selected parameters |
| `report_generator.py`     | Produces summaries and reports                       |
| `app.py`                  | Main application interface                           |

---

# Technologies Used

* **Programming:** Python
* **Data Processing:** Pandas, NumPy
* **Graph Analysis:** NetworkX
* **Visualization:** Matplotlib, Plotly
* **Application Interface:** Streamlit

---

# Installation

Clone the repository:

```bash id="jx7m45"
git clone https://github.com/Ushosree177/Ecoshock.git
```

Move into the project directory:

```bash id="nr5zla"
cd Ecoshock
```

Create and activate a virtual environment:

```bash id="yu3p6o"
python -m venv venv
```

### Windows

```bash id="2i2ese"
venv\Scripts\activate
```

### macOS/Linux

```bash id="321hg8"
source venv/bin/activate
```

Install dependencies:

```bash id="vtg6cd"
pip install -r requirements.txt
```

Run the application:

```bash id="q00lld"
streamlit run app.py
```

---

# Example Workflow

### Step 1: Select or define a crisis

Example:

```text id="naql7h"
Global oil supply disruption
```

### Step 2: Identify the initial shock

```text id="89tbok"
Oil Supply ↓
```

### Step 3: Propagate the shock

```text id="hm7uu4"
Oil Supply Disruption
        │
        ▼
Fuel Prices
        │
        ▼
Transportation Costs
        │
        ▼
Food Distribution
        │
        ▼
Consumer Prices
```

### Step 4: Analyze sector impacts

### Step 5: Analyze social-group impacts

### Step 6: Perform sensitivity analysis

### Step 7: Generate a report

---

# Validation and Evaluation

## Important Note

EcoShock is primarily a **rule-based scenario and decision-support system**, not a conventional supervised machine-learning classifier.

Evaluation should distinguish between:

1. **Structural validation** — whether graph relationships and propagation pathways are economically meaningful.
2. **Historical scenario validation** — whether modeled impact patterns are consistent with historical events.
3. **Quantitative validation** — comparison with explicitly defined real-world observations.
4. **Sensitivity and robustness analysis** — examination of how results change under different assumptions.

## Reproducibility Requirement

Any numerical metric reported for EcoShock should clearly specify:

* the evaluation dataset or source,
* the ground-truth variable,
* the prediction target,
* the time period,
* the metric definition,
* and the evaluation procedure.

For example:

[
\text{MAPE}
===========

\frac{100}{n}
\sum_{t=1}^{n}
\left|
\frac{y_t-\hat{y}_t}{y_t}
\right|
]

where (y_t) is an observed value and (\hat{y}_t) is the corresponding model estimate.

> **Numerical accuracy and MAPE values should only be included when the corresponding ground truth and evaluation procedure are reproducible from the project files.**

---

# Applications

## Government and Public Policy

* Policy stress testing
* Crisis planning
* Subsidy analysis
* Vulnerable-group assessment
* Scenario comparison

## Financial and Economic Analysis

* Macroeconomic scenario analysis
* Sector-risk exploration
* Shock transmission analysis
* Stress-testing research

## Industry and Supply Chains

* Supply-chain disruption analysis
* Commodity shock scenarios
* Business continuity planning
* Sector-dependency analysis

## Education and Research

* Economic networks
* Graph-based modeling
* Explainable decision systems
* Sensitivity analysis
* Scenario simulation

---

# Limitations

EcoShock is an exploratory decision-support and simulation framework.

### Rule Dependence

Results depend on the quality and validity of the specified economic rules and relationships.

### Simplified Economic Structure

Real economies contain feedback loops, nonlinear effects, delays, and complex interactions that may not be fully represented by a simple directed graph.

### Parameter Dependence

Results can change depending on edge weights, propagation rules, and scenario assumptions.

### Not a Causal Identification Framework

The current system should not be interpreted as establishing causal effects in the econometric sense.

### Not a Deterministic Forecasting System

EcoShock generates scenario-based impact assessments and does not guarantee future economic outcomes.

---

# Future Work

Potential extensions include:

### 1. Dynamic Graph Modeling

[
G_t = (V_t, E_t)
]

to allow sector relationships to evolve over time.

### 2. Probabilistic Uncertainty Modeling

Possible approaches:

* Bayesian graph models
* Monte Carlo simulation
* Bayesian networks
* Probabilistic programming

### 3. Data-Driven Parameter Estimation

Estimate graph relationships from real economic data using:

* time-series modeling,
* graphical models,
* causal discovery,
* or Bayesian estimation.

### 4. Hybrid Rule-Based and Machine Learning Models

```text id="59xm7i"
Expert Knowledge
      +
Graph Structure
      +
Historical Data
      +
Machine Learning
      =
Hybrid Economic Decision Support System
```

### 5. Historical Backtesting

Develop a reproducible pipeline with:

* clearly defined scenarios,
* time periods,
* observed variables,
* benchmark models,
* and evaluation metrics.

### 6. Geographic and Policy Analysis

Extend EcoShock to country-, state-, or region-level analysis and model interventions such as subsidies, interest-rate changes, income support, and targeted social protection.

---

# Research Relevance

EcoShock is relevant to:

* Graph-Based Modeling
* Decision Support Systems
* Economic Networks
* Complex Systems
* Explainable Artificial Intelligence
* Scenario Analysis
* Sensitivity Analysis
* Economic Risk Modeling

The project can also serve as a foundation for future work combining **probabilistic modeling and Bayesian uncertainty quantification with graph-based economic shock propagation**.

---

# Citation

```text id="f8bgen"
Raha, U. (2026).
EcoShock: A Graph-Based Economic Shock Propagation and Decision Support System.
GitHub Repository.
https://github.com/Ushosree177/Ecoshock
```

---

# Author

**Ushosree Raha**

M.S. in Artificial Intelligence and Data Science
ABV-Indian Institute of Information Technology and Management, Gwalior

**Research Interests**

Bayesian Statistics · Probabilistic Modeling · Bayesian Machine Learning · Financial Time Series · Graph-Based Modeling · Uncertainty Quantification

* GitHub: https://github.com/Ushosree177
* Portfolio: https://ushosree177.github.io
* LinkedIn: https://www.linkedin.com/in/ushosree-raha-53b75b227/

---

# Project Status

**Active / Research and Development**

EcoShock is an evolving research and software project. The current version focuses on an interpretable rule-based and graph-based framework for economic shock propagation. Future versions may incorporate data-driven estimation, probabilistic uncertainty modeling, and more rigorous historical validation.



