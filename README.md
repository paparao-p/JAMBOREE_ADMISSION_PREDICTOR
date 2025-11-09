# ⭐ JAMBOREE ADMISSION PREDICTOR

This project predicts the **probability of admission** into graduate programs abroad using student academic scores and profile metrics. The dataset used is associated with **Jamboree**, a study-abroad consultancy, and was provided as part of institutional training.

The goal is to understand **which factors influence admission chances** the most, and to build a **stable, interpretable regression model** that can estimate a student’s likelihood of admission.

---

## 🎯 Objective
To develop a machine learning model that predicts **Chance of Admit (0–1)** using:
- Academic performance (GRE Score, TOEFL Score, CGPA)
- Profile strength (SOP, LOR)
- University Rating
- Research Experience

---

## 📦 Dataset Overview

| Feature | Description |
|--------|-------------|
| GRE Score | Standardized graduate exam score |
| TOEFL Score | English language proficiency score |
| CGPA | Undergraduate GPA (scaled 0–10) |
| University Rating | University selectivity score (1–5) |
| SOP | Statement of Purpose strength rating (1–5) |
| LOR | Recommendation Letter strength rating (1–5) |
| Research | Research experience (0 = No, 1 = Yes) |
| Chance of Admit | Admission probability (0–1) |

---

## 🔍 Exploratory Data Analysis Highlights

- **CGPA, GRE, and TOEFL** are the **strongest predictors** of admission.
- **SOP, LOR, and University Rating** provide **moderate support** to the prediction.
- Students with **research experience** show a slightly higher admission probability.
- Most students in this dataset have **medium to high** chances of admission.

---

## 🧠 Modeling Approach

| Model | Purpose |
|-------|---------|
| Linear Regression | Baseline predictive model |
| Ridge Regression (L2 Regularization) | Final model to handle multicollinearity |

### Why Ridge?

GRE, TOEFL, and CGPA measure related academic abilities → they are **highly correlated**.  
Instead of removing important features, **Ridge Regression** stabilizes coefficients and maintains interpretability.

---

## 📈 Model Performance

| Model | R² Score | Interpretation |
|-------|---------|----------------|
| Linear Regression | ~0.82 | Strong predictive fit |
| Ridge Regression | ~0.82 | Same accuracy, more stable coefficients ✅ |

Ridge was selected as the **final model**.

---

## 🔑 Feature Importance (Ridge Coefficients)

