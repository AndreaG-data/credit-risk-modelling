# Credit Risk Modelling in Python

**Probability of Default (PD) · Loss Given Default (LGD) · Exposure at Default (EAD) · Expected Loss**

Personal Data Analytics Project | June – September 2026

## 🇬🇧 English

### Project Overview

This personal project explores the application of statistical modelling and machine learning techniques to credit risk assessment and portfolio expected loss estimation.

Based on historical Lending Club loan data, the project implements an end-to-end credit risk modelling workflow, from data preprocessing and borrower risk scoring to model monitoring and expected loss estimation.

The project was completed as part of a guided Udemy course, with additional work to adapt and debug the notebooks in a more recent Python environment.

### Objectives

- Estimate the Probability of Default (PD) using logistic regression.
- Develop an interpretable credit scorecard.
- Monitor changes in borrower characteristics using the Population Stability Index (PSI).
- Estimate Loss Given Default (LGD) and Exposure at Default (EAD).
- Calculate the Expected Loss (EL) of a loan portfolio.

### Dataset

The analysis uses historical Lending Club loan data (2007–2014), covering 466,285 loans.

The dataset includes borrower characteristics, loan information, credit history, repayment status and recovery information.

The original datasets are not included in this repository.

### Methodology

**1. Data Preparation**

Data cleaning, missing-value handling, feature engineering, categorical encoding, binning and Weight of Evidence (WoE) analysis.

**2. Probability of Default and Credit Scorecard**

A logistic regression model estimates borrower default risk. The model is evaluated using ROC-AUC, Gini and Kolmogorov–Smirnov statistics.

The regression coefficients are then transformed into an interpretable points-based credit scorecard.

**3. Model Monitoring**

The Population Stability Index (PSI) is used to compare the development population with a separate 2015 loan population and identify potential distributional changes.

**4. Loss Given Default**

A two-stage modelling approach combines logistic regression for positive recovery identification with linear regression for recovery rate estimation.

**5. Exposure at Default**

Linear regression estimates a remaining-principal factor used to calculate exposure at default.

**6. Expected Loss Calculation**

Individual expected losses are calculated using:

**Expected Loss = PD × LGD × EAD**

These estimates are then aggregated to obtain the portfolio-level Expected Loss.

### Key Results

| Metric | Result |
|---|---|
| Loans analysed | 466,285 |
| PD model ROC-AUC | 70.18% |
| PD model Gini coefficient | 40.35% |
| PD model KS statistic | 29.68% |
| Overall score PSI | 0.0873 |
| Total funded amount | $6.664 billion |
| Portfolio Expected Loss | $512.44 million |
| Expected Loss / Funded Amount | 7.69% |

These results describe a historical educational modelling exercise, not a production-ready credit risk model.

### Technologies and Skills

**Python · pandas · NumPy · scikit-learn · Logistic Regression · Linear Regression · Statistical Modelling · Credit Scoring · Feature Engineering · Model Evaluation · Data Visualization**

### Repository Contents

- **Data Preparation:** Data cleaning and feature engineering.
- **PD Model:** Probability of Default estimation and credit scorecard.
- **Monitoring:** Population Stability Index analysis.
- **Calculating Expected Loss:** LGD, EAD and portfolio Expected Loss modelling.
- **Credit Risk Modelling Report:** Detailed methodology, results and limitations.

The notebooks require the original input datasets and intermediate data files, which are not provided in this repository.

### Limitations

This project follows a guided educational methodology and does not constitute a fully validated regulatory credit risk framework.

In particular, it does not implement the complete requirements of IFRS 9 or Basel regulatory models. Further calibration, independent validation and temporal robustness assessments would be necessary for real-world deployment.

---

## 🇫🇷 Français

### Présentation du projet

Ce projet personnel explore l'application de méthodes statistiques et de Machine Learning à l'évaluation du risque de crédit et à l'estimation des pertes attendues d'un portefeuille de prêts.

À partir de données historiques de Lending Club, il met en œuvre une chaîne complète de modélisation du risque de crédit, depuis la préparation des données jusqu'à l'estimation des pertes attendues, en passant par le scoring et le suivi des modèles.

Ce projet a été réalisé dans le cadre d'une formation Udemy, avec un travail complémentaire d'adaptation et de débogage des notebooks dans un environnement Python plus récent.

### Objectifs

- Estimer la probabilité de défaut (PD) à l'aide d'une régression logistique.
- Construire une grille de score de crédit interprétable.
- Suivre l'évolution des caractéristiques des emprunteurs avec le Population Stability Index (PSI).
- Estimer la perte en cas de défaut (LGD) et l'exposition au défaut (EAD).
- Calculer la perte attendue (Expected Loss) d'un portefeuille de prêts.

### Données utilisées

L'analyse repose sur les données historiques de Lending Club (2007–2014), comprenant 466 285 prêts.

Ces données regroupent des informations sur les emprunteurs, les caractéristiques des prêts, les historiques de crédit, les remboursements et les recouvrements.

Les fichiers de données d'origine ne sont pas inclus dans ce dépôt.

### Méthodologie

**1. Préparation des données**

Nettoyage, traitement des valeurs manquantes, création de variables, encodage des catégories, regroupement en intervalles et analyse Weight of Evidence (WoE).

**2. Probabilité de défaut et score de crédit**

Estimation du risque de défaut par régression logistique, puis évaluation du modèle à l'aide des indicateurs ROC-AUC, Gini et Kolmogorov–Smirnov.

Les coefficients du modèle sont ensuite convertis en une grille de score interprétable.

**3. Suivi du modèle**

Utilisation du Population Stability Index (PSI) pour comparer les distributions des variables entre la population de développement et une population de prêts de 2015.

**4. Loss Given Default (LGD)**

Modélisation en deux étapes combinant une régression logistique pour identifier les recouvrements positifs et une régression linéaire pour estimer leur montant relatif.

**5. Exposure at Default (EAD)**

Utilisation d'une régression linéaire pour estimer la proportion de capital restant exposée au moment du défaut.

**6. Calcul de la perte attendue**

La perte attendue est estimée pour chaque prêt selon la formule :

**Expected Loss = PD × LGD × EAD**

Les pertes individuelles sont ensuite agrégées à l'échelle du portefeuille.

### Principaux résultats

| Indicateur | Résultat |
|---|---|
| Prêts analysés | 466 285 |
| ROC-AUC du modèle PD | 70,18 % |
| Coefficient de Gini | 40,35 % |
| Statistique KS | 29,68 % |
| PSI global du score | 0,0873 |
| Montant total financé | 6,664 milliards $ |
| Perte attendue du portefeuille | 512,44 millions $ |
| Perte attendue / montant financé | 7,69 % |

Ces résultats correspondent à une étude pédagogique sur des données historiques et ne constituent pas des estimations applicables directement à un portefeuille bancaire actuel.

### Technologies et compétences

**Python · pandas · NumPy · scikit-learn · Régression logistique · Régression linéaire · Modélisation statistique · Scoring crédit · Feature Engineering · Évaluation de modèles · Visualisation de données**

### Contenu du dépôt

- **Data Preparation :** Préparation des données et création des variables.
- **PD Model :** Modélisation de la probabilité de défaut et score de crédit.
- **Monitoring :** Analyse de stabilité avec le PSI.
- **Calculating Expected Loss :** Modélisation LGD, EAD et calcul de la perte attendue.
- **Credit Risk Modelling Report :** Rapport détaillant la méthodologie, les résultats et les limites.

L'exécution des notebooks nécessite les données d'origine et certains fichiers intermédiaires, qui ne sont pas fournis dans ce dépôt.

### Limites

Ce projet constitue un exercice pédagogique de modélisation du risque de crédit et non un modèle réglementaire entièrement validé.

Il ne couvre pas l'ensemble des exigences des cadres IFRS 9 ou Bâle. Une application réelle nécessiterait notamment des analyses complémentaires de calibration, de validation indépendante et de robustesse temporelle.
