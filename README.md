# 📊 Customer Segmentation Using Hybrid Clustering (KM\_AE)

A capstone project focused on optimizing retail marketing strategies through intelligent customer segmentation using RFM data and hybrid ML techniques. This includes a fully interactive Streamlit dashboard to explore segment-wise trends and visualize the clustering outcomes.
https://km-ae-dashboard.streamlit.app/

---

## 🚀 Project Summary

This project applies both **baseline (PCA + Clustering)** and **advanced (AutoEncoder + Clustering)** models on RFM-engineered customer behavior data. After evaluating six model variants on performance, interpretability, and robustness, we selected **AutoEncoder + KMeans (KM\_AE)** for its superior clustering quality and practical marketing relevance.

Dataset: **Online Retail II** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii)

---

## ✅ Model Comparison & Final Selection

| Model Variant | Silhouette | Stability | Interpretability |
| ------------- | ---------- | --------- | ---------------- |
| KM\_PCA       | 0.48       | Moderate  | High             |
| GMM\_PCA      | 0.45       | Moderate  | Medium           |
| AGGLO\_PCA    | 0.47       | Low       | Medium           |
| **KM\_AE** ✅  | **0.62**   | High      | Medium           |
| GMM\_AE       | 0.59       | High      | Low              |
| AGGLO\_AE     | 0.55       | Moderate  | Medium           |

**Why KM\_AE?**

* Highest Silhouette Score (0.62)
* Cluster separation validated via ANOVA + Tukey HSD
* Resilient under Gaussian noise & feature ablation
* Best blend of business interpretability + technical robustness

📚 *Inspired by*:

* Gupta et al. (2024), *Hybrid Autoencoder-GMM Segmentation*, IJDSA
* Sarkar et al. (2024), *AI in Marketing Optimization*, JBMS

---

## 📈 Business Impact

### Cluster Personas:

* **Cluster 0**: Low-value, low-frequency — deprioritize
* **Cluster 1**: High-value, frequent buyers (VIP) — retain & reward
* **Cluster 2**: Infrequent, high-value — re-engagement campaigns

### Modeled KPI Outcomes:

| Metric                   | Estimated Value |
| ------------------------ | --------------- |
| Retention improvement    | +15%            |
| Campaign ROI uplift      | +18%            |
| Cost-per-conversion drop | −12%            |
| Annual marketing savings | \$50K–\$75K CAD |

🌟 Based on insights from:

* McKinsey (2021): [Getting Personalization Right](https://www.mckinsey.com/business-functions/growth-marketing-and-sales/our-insights/the-value-of-getting-personalization-right-or-wrong)
* Deloitte Digital (2020): CPA reduction through behavioral targeting
* Shopify Case Study: 5–10% lift in conversions → \$50K+ ROI

---

## 📊 Dashboard Features (Streamlit)

* RFM Score Distribution by Cluster
* Cluster-wise Customer Count Bar Charts
* Heatmap: Avg R, F, M per Cluster
* t-SNE Visualizations for Separation
* ROI Impact Scenario Graphs

---

## ⚙️ Run Locally

1. Clone this repo
2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Run the Streamlit dashboard

```bash
streamlit run customer_segmentation_dashboard.py
```

Make sure your data files (`rfm_with_km_ae.csv`, `tsne_with_km_ae.csv`) are in the working directory.

---

## 👨‍💻 Contributors

* **S. Vignesh**
* **Vayisnavei Gnanamanogaran**
  Ontario Tech University – 2025

---

