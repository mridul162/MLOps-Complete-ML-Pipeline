# 🚀 Production-Ready MLOps Pipeline with DVC, DVCLive & AWS S3

> End-to-end machine learning pipeline with **reproducibility, experiment tracking, and cloud integration**, following real-world MLOps practices.

---

## 📌 Project Highlights

* ⚙️ Built a **modular ML pipeline** with reusable components (`src/`)
* 🔁 Ensured **full reproducibility** using DVC pipelines (`dvc.yaml`)
* 📊 Enabled **experiment tracking & comparison** using DVCLive + DVC Experiments
* 🧪 Implemented **parameterized workflows** via `params.yaml`
* ☁️ Integrated **AWS S3 as remote storage** for data & models
* 🔄 Designed a **Git + DVC hybrid versioning system**
* 📉 Structured outputs: metrics, reports, and artifacts

---

## 🧠 Why This Project Matters

In real-world ML systems:

* Code alone is **not sufficient**
* Data and models must be **versioned**
* Experiments must be **tracked & reproducible**
* Pipelines must be **automated and scalable**

This project demonstrates all of the above in a **production-aligned workflow**.

---

## 🏗️ Architecture Overview

```
                ┌──────────────┐
                │  params.yaml │
                └──────┬───────┘
                       │
                ┌──────▼───────┐
                │  dvc.yaml    │
                │ (Pipeline)   │
                └──────┬───────┘
                       │
        ┌──────────────┼────────────────┐
        │              │                │
   Data Ingestion   Training       Evaluation
        │              │                │
        └────► Artifacts & Metrics ◄────┘
                       │
                 DVCLive Logs
                       │
                DVC Experiment
                       │
                AWS S3 Remote
```

---

## 📂 Project Structure

```
.
├── src/                # Modular pipeline components
├── data/               # Input datasets (DVC tracked)
├── models/             # Trained models
├── reports/            # Metrics, plots, outputs
├── dvc.yaml            # Pipeline stages
├── dvc.lock            # Pipeline reproducibility snapshot
├── params.yaml         # Hyperparameters
├── dvclive/            # Experiment logs
├── requirements.txt
└── README.md
```

---

## ⚙️ Core Workflow

### 🔹 Run Full Pipeline

```bash
dvc repro
```

Executes all stages with dependency tracking.

---

### 🔹 Modify Parameters

Edit:

```
params.yaml
```

Re-run:

```bash
dvc repro
```

---

### 🔹 Track Experiments

```bash
dvc exp run
dvc exp show
```

Compare:

* Metrics
* Parameters
* Performance trends

---

### 🔹 Reproduce Past Experiments

```bash
dvc exp apply <exp-name>
```

---

### 🔹 Visualize Pipeline

```bash
dvc dag
```

---

## ☁️ Cloud Integration (AWS S3)

* Configured S3 as **remote artifact store**
* Enables:

  * Team collaboration
  * Scalable storage
  * Centralized data access

```bash
aws configure
dvc remote add -d dvcstore s3://<bucket-name>
dvc push
```

---

## 🔄 Versioning Strategy

| Component   | Tool          |
| ----------- | ------------- |
| Code        | Git           |
| Data        | DVC           |
| Models      | DVC           |
| Pipeline    | DVC           |
| Experiments | DVC + DVCLive |

---

## 📊 Example Use Cases

* Reproducible ML experiments
* Team-based ML development
* Model lifecycle management
* Data-centric ML workflows

---

## 🛠️ Tech Stack

* **Languages:** Python
* **ML:** Scikit-learn / TensorFlow (customizable)
* **MLOps:** DVC, DVCLive
* **Cloud:** AWS S3
* **Versioning:** Git + GitHub

---

## 📈 What This Demonstrates (For Recruiters)

✅ Understanding of **MLOps lifecycle**
✅ Ability to build **reproducible pipelines**
✅ Hands-on experience with **DVC ecosystem**
✅ Knowledge of **experiment tracking & comparison**
✅ Cloud integration (**AWS S3**)
✅ Clean project structuring for **scalability**

---

## 🚀 How to Run Locally

```bash
git clone <repo-url>
cd <repo>

pip install -r requirements.txt

dvc init
dvc repro
```

---

## 📬 Contact

* GitHub: *[your profile link]*
* LinkedIn: *[your profile link]*

---

## ⭐ Final Note

This project is built with a **production mindset**, not just experimentation.
It reflects how ML systems are developed in **real-world environments**, bridging the gap between:

> **"I can build models" → "I can deploy and manage ML systems"**

---
