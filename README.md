# ⚖️ AI Fairness Checker – Unbiased AI Decision

**Live Demo:** [https://pankajyadav098765.github.io/unbiased-ai-decision/](https://pankajyadav098765.github.io/unbiased-ai-decision/)

An interactive web tool that audits AI models for **bias and discrimination** using three industry‑standard fairness metrics.  
Built for the **"Unbiased AI Decision – Ensuring Fairness and Transparency"** challenge.

---

## 🎯 What It Does

- Detects bias in AI decision‑making (loan approvals, hiring, admissions, etc.)
- Works entirely in the browser – no backend, no installation.
- Upload a CSV with two columns: `decision` (0/1) and `protected` (two groups).
- Instantly computes fairness metrics and shows a clear verdict.

---

## 📊 Fairness Metrics

| Metric | Description | Fairness Threshold |
|--------|-------------|---------------------|
| **Statistical Parity Difference (SPD)** | Difference in approval rates between groups | `|SPD| < 0.1` |
| **Disparate Impact Ratio (DIR)** | Ratio of approval rates (`P(Yes|Group1) / P(Yes|Group0)`) | `0.8 – 1.25` |
| **Equalized Odds (TPR Difference)** | Difference in True Positive Rates | `|TPR diff| < 0.1` |

- ✅ **FAIR** – All three metrics within fair range  
- ⚠️ **MODERATELY UNFAIR** – Slight bias detected  
- 🚨 **UNFAIR – Strong Bias** – Severe disparity

---

## 📁 Sample CSV Files

Download and test with these prepared datasets:

| File | Description | Result |
|------|-------------|--------|
| [`fair.csv`](./fair.csv) | Perfectly balanced (60% approvals both groups) | ✅ **FAIR** |
| [`unfair.csv`](./unfair.csv) | 90% Male vs 10% Female approvals | 🚨 **UNFAIR** |

**CSV format:**  
```csv
decision,protected
1,Male
0,Female
...
