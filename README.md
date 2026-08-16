# Flight Delay Prediction

> **An applied Machine Learning regression study focused on predicting flight delays from historical flight data and producing a reusable trained-model artifact.**

This project explores the end-to-end workflow of a supervised regression problem: understanding the available flight data, preparing features, training and evaluating a predictive model, and persisting the final model for later use.

<p>
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white" alt="Jupyter">
  <img src="https://img.shields.io/badge/Machine%20Learning-Regression-green" alt="Machine Learning Regression">
</p>

---

## The problem

Flight delays affect passengers, airlines, airports, and operational planning.

From a Data Science perspective, the problem can be framed as:

> **Can historical flight information be used to estimate the expected delay of a flight?**

The project treats delay prediction as a regression task and organizes the work around the typical lifecycle of an applied Machine Learning experiment.

---

## Workflow

```text
Historical Flight Data
        ↓
Data Exploration
        ↓
Data Preparation
        ↓
Feature Engineering
        ↓
Regression Modeling
        ↓
Model Evaluation
        ↓
Final Model Selection
        ↓
Serialized Model Artifact
```

---

## What this project demonstrates

- framing an operational problem as supervised Machine Learning;
- exploratory analysis of tabular data;
- preparation of features for regression;
- model training and evaluation;
- interpretation of prediction errors;
- selection of a final model;
- persistence of a trained model as a reusable artifact;
- separation between the experimentation notebook and the resulting model file.

---

## Repository artifacts

| Artifact | Purpose |
|---|---|
| [`flights.csv`](./flights.csv) | Historical dataset used in the study |
| [`Previsibilidade_nos_atrasos_de_voos.ipynb`](./Previsibilidade_nos_atrasos_de_voos.ipynb) | Complete analysis and modeling workflow |
| [`modelo_producao.pkl`](./modelo_producao.pkl) | Serialized final model produced by the experiment |

---

## Model lifecycle represented in the project

The notebook represents the experimentation stage of a predictive solution:

```text
Data
 ↓
Experimentation
 ↓
Evaluation
 ↓
Selected Model
 ↓
Serialization (.pkl)
```

The presence of the serialized artifact is useful because it separates **training** from **later inference**, even though this repository does not include a production API or online serving layer.

---

## Running the study

Clone the repository:

```bash
git clone https://github.com/rodrigorissettoterra/Previsao-de-atraso-em-voos.git
cd Previsao-de-atraso-em-voos
```

Open the notebook with Jupyter:

```bash
jupyter notebook Previsibilidade_nos_atrasos_de_voos.ipynb
```

The exact environment used when the serialized model was generated should be reproduced when loading `modelo_producao.pkl`, because Python model artifacts may depend on compatible library versions.

---

## Limitations

This repository represents an applied Machine Learning study rather than a complete production prediction service.

Current limitations include:

- no real-time data ingestion;
- no prediction API;
- no model registry or experiment tracking;
- no automated retraining pipeline;
- no monitoring for feature or prediction drift;
- model behavior is constrained by the historical data used during training.

A production implementation would need to address these operational concerns in addition to predictive performance.

---

## Possible next steps

The project could evolve toward a production-oriented architecture with:

- reproducible dependency management;
- experiment tracking;
- model versioning;
- FastAPI-based serving;
- containerization;
- automated tests;
- drift and performance monitoring;
- scheduled or event-driven retraining.

---

## Author

**Rodrigo Terra**

Data & AI professional focused on Data Science, Analytics Engineering, Artificial Intelligence, and reliable data-driven systems.

- GitHub: [Rodrigo Terra](https://github.com/rodrigorissettoterra)
- LinkedIn: [Rodrigo Terra](https://www.linkedin.com/in/rodrigo-rissetto-terra/)
