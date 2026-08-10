# Telecom Customer Churn Analysis & Commercial Strategy for Banglalink

This repository provides an end-to-end Machine Learning and Exploratory Data Analysis (EDA) pipeline for predicting subscriber churn in the telecommunications sector. 

While the baseline analytical framework is established using the industry-standard **IBM Telco Customer Churn Dataset**, the insights, feature mappings, and model outputs are translated into actionable, commercial strategy recommendations for **Banglalink**.

---

## 📌 Business Overview & Core Insights

Customer retention is a primary growth engine in modern telecom. Identifying high-risk subscriber segments allows commercial teams to deploy targeted retention campaigns before attrition occurs. 

Key findings from the analysis:

* **High-Risk Onboarding Window (0–6 Months):** Subscriber churn reaches **~53.8%** during the initial 6 months of tenure before steadily dropping in later cohorts.
* **Streaming User Vulnerability:** Active streaming users churn at **~30%**, compared to **~23%** for non-streamers—a **7 percentage point increase**. Video traffic users are particularly sensitive to network Quality of Experience (QoE) and data costs.
* **Revenue Risk in Month-to-Month Contracts:** Flexible/uncommitted subscribers account for **over 80%** of total lost monthly revenue among churned users.
* **Payment Channel Disparity:** Subscribers using physical scratchcards and manual payment methods show significantly higher churn compared to those using digital, automated payment channels.

---

## 🛠️ Commercial Strategy Recommendations (Banglalink)

| Strategy Pillar | Data Finding | Actionable Commercial Initiative |
| :--- | :--- | :--- |
| **Structured Onboarding (0–90 Days)** | Churn peaks sharply (**~53.8%**) in the `0-6 Mo` cohort. | Deploy automated **MyBL App notifications** delivering Day-30 and Day-60 bonus data boosters for newly activated SIMs to drive habituation. |
| **Toffee QoE & Bundle Optimization** | Streamers exhibit **7% higher churn** than non-streamers. | Introduce zero-rated or discounted **Toffee streaming data passes** combined with video-specific network Quality of Service (QoS) optimizations. |
| **Digital Recharge Incentives** | Manual recharges correlate with higher churn probabilities. | Offer a 5% cashback or bonus data allowance when subscribers recharge via **MyBL, bKash, or Nagad auto-pay**. |
| **Micro-Commitment Packs** | Uncommitted subscribers drive **>80%** of total lost monthly revenue. | Launch discounted **3-month micro-commitment bundles** to transition pay-as-you-go users into stable recurring revenue streams. |

---

## 🔄 Dataset Context & Adaptability to Native Banglalink Data

> **Baseline Dataset:** This analysis relies on the **IBM Telco Customer Churn Dataset**, an industry benchmark dataset used to train baseline classification models (Logistic Regression, Random Forest, XGBoost) and establish analytical pipelines.

When adapted to native **Banglalink subscriber data**, this framework seamlessly ingests internal data sources:



```
              +-----------------------------------+
              | Native Banglalink Data Sources    |
              +-----------------------------------+
                                |
 +------------------------------+------------------------------+
 |                              |                              |
 v                              v                              v


[ CDR & Network Logs ]     [ MyBL App Analytics ]      [ Billing & Recharge Logs ]

* Toffee Watch Time        - App Engagement            - bKash/Nagad vs. Scratchcard
* Video Buffer Rates       - Active Pass Types         - Recharge Frequency & ARPU
|                              |                              |
+------------------------------+------------------------------+
|
v
+-----------------------------------+
|  Production ML Churn Pipeline     |
+-----------------------------------+

```

---

## 🚀 Getting Started

### Prerequisites

* Python 3.8+
* Jupyter Notebook or JupyterLab

### Installation

1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/banglalink-churn-analysis.git](https://github.com/your-username/banglalink-churn-analysis.git)
   cd banglalink-churn-analysis

```

2. Install required dependencies:
```bash
pip install -r requirements.txt

```


3. Launch the Jupyter Notebook:
```bash
jupyter notebook

```



---

## 📂 Project Structure

```
.
├── data/
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv   # IBM Telco Dataset
├── notebooks/
│   └── Churn_Analysis.ipynb        # Main EDA and Modeling Notebook
├── models/
│   └── churn_classifier.pkl                   # Trained ML model pipeline
├── README.md                                  # Project documentation
└── requirements.txt                           # Python dependencies

```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

```

```
