# 🌍 EcoShock

## Economic Impact Analysis & Decision Support System

EcoShock is a rule-based Decision Support System (DSS) that analyzes how global crises such as wars, pandemics, fuel shortages, recessions, and natural disasters affect different economic sectors and social classes.

The system uses graph propagation, expert-defined rules, and sensitivity analysis to simulate economic shock transmission without requiring machine learning models, APIs, or external datasets.

---

## 📌 Features

### 1. Crisis Impact Simulation

Analyze the economic impact of:

* Russia–Ukraine War
* COVID-19 Pandemic
* Global Fuel Crisis
* Global Recession
* US–China Trade War
* Custom user-defined scenarios

---

### 2. Sector Analysis

The system evaluates impacts on:

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

---

### 3. Social Class Impact Analysis

EcoShock estimates crisis effects on:

* Rich
* Upper Middle Class
* Lower Middle Class
* Poor

This helps identify which groups suffer the most during economic disruptions.

---

### 4. Graph-Based Shock Propagation

The system models the economy as a weighted Directed Acyclic Graph (DAG).

Example:

Global Event → Petrol → Transport → Food → Living Cost → Social Classes

This allows economic shocks to propagate realistically through interconnected sectors.

---

### 5. Custom Scenario Engine

Users can enter free-text crisis descriptions such as:

"Major earthquake causing infrastructure collapse"

or

"Global oil supply disruption"

The system automatically identifies keywords and generates impact predictions.

---

### 6. Sensitivity Analysis

Users can modify:

* Oil Price Increase
* Food Supply Disruption
* Unemployment Rate
* Currency Depreciation
* Interest Rate Changes

and instantly observe their effects on all sectors.

---

### 7. Automated Reporting

Generate:

* Economic impact reports
* Sector summaries
* Social class assessments
* Exportable results

---

## 🏗️ System Architecture

### Layer 1: Expert Knowledge Base

Contains:

* Economic rules
* Sector relationships
* Historical crisis impacts

### Layer 2: Graph Propagation Engine

Uses:

* NetworkX
* Topological Sorting
* Weighted DAG Traversal

to propagate shocks across the economy.

---

## 🛠️ Technologies Used

* Python
* Streamlit
* NetworkX
* Pandas
* NumPy
* Matplotlib
* Plotly

---

## 📂 Project Structure

```bash
EcoShock/
│
├── app.py
├── requirements.txt
├── data/
├── reports/
├── assets/
├── modules/
│   ├── graph_engine.py
│   ├── scenario_engine.py
│   ├── sensitivity_analysis.py
│   └── report_generator.py
│
└── README.md
```

---

## 📊 Validation Results

The system was validated using real-world economic events.

| Event                     | Accuracy |
| ------------------------- | -------- |
| Russia–Ukraine War (2022) | 91.1%    |
| COVID-19 Pandemic (2020)  | 92.0%    |
| Global Fuel Crisis (2022) | 91.0%    |
| Overall Accuracy          | 91.4%    |

Average MAPE: **8.61%**

---

## 🎯 Applications

### Government

* Policy planning
* Subsidy targeting
* Economic stress testing
* Crisis management

### Financial Sector

* Portfolio risk analysis
* Credit risk assessment
* Investment strategy planning

### Education

* Economics learning
* Research projects
* Public policy studies

### Industry

* Supply chain risk monitoring
* Business continuity planning
* Market impact assessment

---

## 📈 Future Improvements

* Machine Learning Hybrid Model
* Live Economic Data Integration
* LLM-Based Scenario Understanding
* State-Level Economic Analysis
* Multi-Country Support
* Mobile Application
* Policy Recommendation Engine

---

## 📄 Research Paper

**EcoShock: A Rule-Based Graph Propagation Decision Support System for Multi-Sector Economic Impact Analysis Across Social Classes**

Author: Ushosree Raha

ABV-Indian Institute of Information Technology and Management (ABV-IIITM), Gwalior

---

## 👨‍💻 Author

**Ushosree Raha**

MS (Artificial Intelligence & Data Science)

ABV-IIITM Gwalior



