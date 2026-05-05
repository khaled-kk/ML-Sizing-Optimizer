# 👕 ML Sizing Optimizer: K-Means Apparel Classification

[![ML: Scikit-Learn](https://img.shields.io/badge/ML-Scikit--Learn-orange.svg)]()
[![Domain: Manufacturing](https://img.shields.io/badge/Domain-Smart--Manufacturing-blue.svg)]()
[![Status: Complete](https://img.shields.io/badge/Status-Complete-success.svg)]()

**ML Sizing Optimizer** is a machine learning project that automates the categorization of apparel sizes using K-Means Clustering. By analyzing high-dimensional physical measurements, the system identifies optimal clusters to streamline manufacturing and inventory management.

## 🎯 Project Objective
Traditional sizing often fails to capture the complexity of human proportions. This project uses unsupervised learning to group complex measurement sets—including sleeve length, neck size, and shoulder width—into $K$ logical categories, ensuring better fit and reduced manufacturing waste.

## 📊 Features & Data Dimensions
The model processes five critical dimensions to determine the ideal cluster:
1. **Height & Width:** Core body proportions.
2. **Sleeve Length:** Arm-to-torso ratio.
3. **Neck Size:** Critical for comfort and fastening.
4. **Shoulder Length:** The primary anchor point for apparel fit.

## 🛠 Technical Implementation
* **Algorithm:** K-Means Clustering for unsupervised grouping.
* **Optimization:** [Mention if you used the Elbow Method or Silhouette Score] to determine the optimal number of clusters ($K$).
* **Preprocessing:** Feature scaling (StandardScaler) to ensure all measurement units contribute equally to the distance metrics.



## 📈 Impact on Manufacturing
* **Automated Sizing:** Replaces manual estimation with data-driven categories (e.g., Small, Medium, Large).
* **Inventory Efficiency:** Identifies which size clusters have the highest density, helping brands focus production on the most common body types.
* **Reduced Waste:** Optimizes fabric cutting patterns based on statistically accurate size profiles.

## 🚀 Getting Started
1. **Clone:** `git clone https://github.com/khaled-kk/ML-Sizing-Optimizer.git`
2. **Install Dependencies:** `pip install -r requirements.txt`
3. **Run Analysis:** `python clustering_main.py`

---
*Developed by Khaled Walid*
