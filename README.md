# 🧪 Soft-Sensor for RON Prediction & Evaluation
> **FR:** Soft-Sensor pour la prédiction et l'évaluation de l'indice d'octane (RON)  
> **EN:** Soft-Sensor for Predicting and Evaluating Research Octane Number (RON)

---

## 🇫🇷 Français

### 📝 Description du Projet
Ce projet consiste à concevoir un **Capteur Logiciel (Soft-Sensor)** basé sur l'apprentissage automatique (Machine Learning) pour prédire et évaluer l'indice d'octane (**RON - Research Octane Number**) en temps réel. 

En se basant sur les variables du procédé (Température, Pression, Débit), le modèle permet d'estimer la qualité du produit sans attendre les résultats des analyses de laboratoire, optimisant ainsi le processus de raffinage.

---

### 📊 Explorations des Données (Dataset Summary)
* **Temp_C (Température) :** Moyenne $543.87^\circ C$, Écart-type $31.14$, Plage [$501.70 - 599.90$]
* **Pres_bar (Pression) :** Moyenne $3.28 \text{ bar}$, Écart-type $4.43$, Plage [$1.00 - 23.10$]
* **Flow_m3h (Débit) :** Moyenne $131.10 \text{ m}^3/h$, Écart-type $23.29$, Plage [$85.90 - 159.50$]
* **RON (Indice d'octane) :** Moyenne $9.06$, Écart-type $27.44$, Plage [$0 - 98.80$]

---

### ⚙️ Modélisation & Résultats

#### 1. Modèle de Régression (Linear Regression)
Utilisé pour la prédiction continue de la valeur de **RON** :
* **RMSE (Root Mean Squared Error) :** `1.0626`
* **R² Score :** `0.9986`

#### 2. Modèle de Classification (Decision Tree - `max_depth=3`)
Utilisé pour classifier la conformité du produit selon la règle : $\text{RON} \ge 95$.
* **Précision globale (Accuracy) :** `100% (1.00)`

| Classe | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| **0 (Non conforme)** | 1.00 | 1.00 | 1.00 | 39 |
| **1 (Conforme)** | 1.00 | 1.00 | 1.00 | 3 |
| **Accuracy** | | | **1.00** | 42 |

---

## 🇬🇧 English

### 📝 Project Overview
This project focuses on building a Machine Learning-based **Soft-Sensor** to predict and evaluate the **Research Octane Number (RON)** in real-time.

By using operational process variables (Temperature, Pressure, Flow Rate), the system estimates product quality instantly without waiting for slow laboratory analysis, optimizing refining efficiency.

---

### 📊 Dataset Summary
* **Temp_C (Temperature):** Mean $543.87^\circ C$, Std $31.14$, Range [$501.70 - 599.90$]
* **Pres_bar (Pressure):** Mean $3.28 \text{ bar}$, Std $4.43$, Range [$1.00 - 23.10$]
* **Flow_m3h (Flow Rate):** Mean $131.10 \text{ m}^3/h$, Std $23.29$, Range [$85.90 - 159.50$]
* **RON (Octane Rating):** Mean $9.06$, Std $27.44$, Range [$0 - 98.80$]

---

### ⚙️ Modeling & Results

#### 1. Regression Model (Linear Regression)
Used for continuous prediction of **RON** values:
* **RMSE (Root Mean Squared Error):** `1.0626`
* **R² Score:** `0.9986`

#### 2. Classification Model (Decision Tree - `max_depth=3`)
Used to classify product compliance based on the rule: $\text{RON} \ge 95$.
* **Overall Accuracy:** `100% (1.00)`

| Class | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| **0 (Non-compliant)** | 1.00 | 1.00 | 1.00 | 39 |
| **1 (Compliant)** | 1.00 | 1.00 | 1.00 | 3 |
| **Accuracy** | | | **1.00** | 42 |

---

## 🛠️ Tech Stack / Technologies Utilisées
* **Language:** Python
* **Libraries:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`
