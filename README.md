# :bar_chart: Data Mining (MD) - Polish Bankruptcy

  - [:clipboard: Project Summary](#clipboard-project-summary)
  - [:chart_with_upwards_trend: Key Results](#chart_with_upwards_trend-key-results)
  - [:mag: Scope of the Work](#mag-scope-of-the-work)
    - [:one: Actividad #1](#one-actividad-1)
    - [:two: Actividad #2](#two-actividad-2)
  - [:toolbox: Repository Contents](#toolbox-repository-contents)
  - [:gear: Installation Guide](#gear-installation-guide)
    - [:zero: Prerequisites](#zero-prerequisites)
    - [:one: How to Use the Workflows](#one-how-to-use-the-workflows)

### :busts_in_silhouette: Authors:
  - Sánchez Troncoso, Pablo

---

## :clipboard: Project Summary

This repository contains **two data mining assignments** developed as part of a Bachelor's degree course, focused on predicting corporate bankruptcy using **real-world financial data from Polish companies**.

The project leverages the [Polish Companies Bankruptcy Dataset](https://archive.ics.uci.edu/dataset/365/polish+companies+bankruptcy+data) from the UCI Machine Learning Repository and applies a range of predictive modeling techniques within the KNIME Analytics Platform. The core objective is to build models capable of forecasting whether a company will go bankrupt across five different time horizons: 1, 2, 3, 4, and 5 years.

---

### :chart_with_upwards_trend: Key Results

The models achieve **strong and consistent predictive performance**, reaching **ROC-AUC values above 0.95 for the bankruptcy** (minority) class in the 5-year prediction horizon, evaluated using 10-fold cross-validation. These results indicate a **high level of robustness** in detecting long-term bankruptcy risk despite class imbalance and increasing temporal uncertainty.

**View [lab reports](Actividad_2_Informe_redacted.pdf) for more information.**


---

## :mag: Scope of the Work

The project is divided into two main activities:

### :one: Actividad #1:

Development of a unified predictive workflow that processes multiple datasets (one per time horizon) and generates five independent predictions per company. The workflow includes:
  - Exploratory Data Analysis (EDA)
  - Data preprocessing (shared across datasets)
  - Implementation and evaluation of two predictive models
  - Performance comparison using ROC curves across all time horizons
  - Structured following the CRISP-DM methodology

### :two: Actividad #2:

Extension of the predictive framework with a more advanced and automated pipeline, incorporating:
Comprehensive preprocessing (normalization, missing values, outliers, oversampling, and feature selection)
Wrapper-based feature selection using Naive Bayes optimized for ROC AUC
Implementation of five predictive techniques:
  - Decision Tree
  - Boosting (Decision Tree-based)
  - Bagging (Decision Tree-based)
  - Random Forest
  - Blending (ensemble of previous methods)
  - Stratified 10-fold cross-validation and systematic model evaluation across all prediction horizons

---

### :toolbox: Repository Contents
- [`Actividad_1_Workflow.knwf`](Actividad_1_Workflow.knwf) – KNIME workflow for Activity 1
- [`Actividad_2_Workflow.knwf`](Actividad_2_Workflow.knwf) – KNIME workflow for Activity 2
- [`Actividad_1_Informe_redacted.pdf`](Actividad_1_Informe_redacted.pdf) – Technical report for Activity 1
- [`Actividad_2_Informe_redacted.pdf`](Actividad_2_Informe_redacted.pdf) – Technical report for Activity 2

---

## :gear: Installation Guide

### :zero: Prerequisites

To run this project, you only need to have [KNIME Analytics Platform installed](https://www.knime.com/downloads):

No additional libraries, extensions, or programming environments are required beyond the standard KNIME installation used in the workflows.

### :one: How to Use the Workflows

  1. Open **KNIME Analytics Platform**
  2. Go to `File` → `Import KNIME Workflow`
  3. Select the desired workflow file from this repository:
     - [`Actividad_1_Workflow.knwf`](Actividad_1_Workflow.knwf)
     - [`Actividad_2_Workflow.knwf`](Actividad_2_Workflow.knwf)
  4. Confirm the import and wait for KNIME to load all nodes and dependencies
  5. Open the workflow and execute it using:
  6. `Execute All` (to run the full pipeline), or `Select` specific nodes if step-by-step execution is preferred

Note: Each workflow is designed to automatically read datasets from a folder structure following the assignment format (e.g., `1year.arff`, `2year.arff`, etc.), so no manual preprocessing of the data files is required before execution.

---
