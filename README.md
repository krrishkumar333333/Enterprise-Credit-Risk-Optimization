# 🏦 Enterprise Credit Risk & Portfolio Optimization Engine

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![XGBoost](https://img.shields.io/badge/XGBoost-EWS-red)
![SciPy](https://img.shields.io/badge/SciPy-SLSQP_Optimizer-green)
![Status](https://img.shields.io/badge/Status-Production_Ready-success)

## 📌 Executive Summary
This repository contains a production-grade machine learning and capital allocation pipeline designed to optimize a retail digital lending portfolio. Built originally for the **IIT Guwahati Consulting & Analytics Competition**, this engine ingests empirical borrower data and mathematically synthesizes enterprise business dimensions (CAC, Turnaround Times, and Macroeconomic spending shocks) to create a highly constrained, real-world credit environment.

## ⚙️ Core Architecture

This project bridges the gap between predictive machine learning and corporate finance by utilizing a dual-engine architecture:

1. **The Early Warning System (XGBoost):** A gradient-boosted classification engine trained on the *Home Credit Default Risk* dataset. It utilizes dynamic class weighting (`scale_pos_weight`) to output Continuous Probabilities of Default (PD) while strictly avoiding target leakage at origination.
2. **The Capital Allocation Engine (SciPy SLSQP):** A calculus-driven optimizer that maximizes risk-adjusted yield. It enforces a strict **3% portfolio concentration limit (HHI Index)** and calculates **Dynamic Loss Given Default (LGD)** based on product type and ticket size.

### 🧮 True Net-Margin Calculus
Unlike academic models that optimize for gross yield (The "Yield Trap"), this engine optimizes for **True Corporate Net Margin**. It explicitly hardcodes:
* **Cost of Funds (CoF):** `6.0%`
* **Operating Expenses (Opex):** `2.5%`
* **Target Margin:** `5.0%`

$$E(R) = (1 - PD) \cdot \text{Yield} - (PD \cdot LGD_{dynamic})$$

## 📊 Strategic Business Outcomes

* **Risk-Based Pricing:** Identified exact retail interest rates required to maintain a 5% net corporate margin across 4 distinct behavioral clusters (e.g., *Prime Stable* vs. *Overleveraged*).
* **Acquisition Economics:** Quantified the trade-off between Customer Acquisition Cost (CAC), Approval Turnaround Time (TAT), and portfolio default rates across distinct marketing channels.
* **Product Strategy:** Mathematically penalized high-ticket, Unsecured Personal Loans vs. BNPL products to protect capital reserves during macroeconomic drawdowns.

## 🚀 How to Run the Pipeline

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YourUsername/Digital-Lending-Optimization.git](https://github.com/YourUsername/Digital-Lending-Optimization.git)
