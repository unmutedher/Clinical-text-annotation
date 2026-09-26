# Medical Coding & Pharmacovigilance Dataset (MedDRA Triage)

This repository contains a text classification dataset designed for clinical trial eligibility screening and adverse event triage. The data has been annotated using **doccano** and structured according to standard global medical categories.

## 🚀 Project Overview
The objective of this project is to process raw clinical notes and categorize them based on the **MedDRA (Medical Dictionary for Regulatory Activities)** hierarchy at the **System Organ Class (SOC)** level. Additionally, the dataset flags patients who present immediate safety risks that disqualify them from trial enrollment.

## 📊 Dataset Format
The data is stored in **JSONL (JSON Lines)** format. Each row represents a single patient clinical text snippet structured as follows:

```json
{"text": "Patient diagnosed with invasive ductal carcinoma...", "label": ["MedDRA_SOC_NEOPLASMS"]}
```

## 🏷️ Label Dictionary

| Label Name | MedDRA Classification / Logic | Clinical Mapping Criteria |
| :--- | :--- | :--- |
| **`MedDRA_SOC_NEOPLASMS`** | Tumors, Cancers, & Growths | Applied to carcinomas, sarcomas, leukemias, and metastatic masses. |
| **`MedDRA_SOC_BLOOD_LYMPHATICS`** | Hematological Disorders | Applied to severe cytopenias (neutropenia, thrombocytopenia) and lymph node disorders. |
| **`MedDRA_SOC_RESPIRATORY`** | Respiratory System | Applied to direct lung pathologies, chronic cough, dyspnea, or pneumonitis. |
| **`INELIGIBLE_EXCLUSION_CRITERIA`** | Trial Disqualification Signal | Toggled for life-threatening toxicities, severe organ failure (e.g., AKI), or active clinical emergencies. |

## 🛠️ Tools Used
* **Annotation Platform:** [doccano](https://github.com) (Open-source text annotation tool)
* **Data Schema:** JSONL (JSON Lines)
# Clinical-text-annotation
Clinical text annotation and triage datasets using doccano, structured according to MedDRA System Organ Class (SOC) guidelines for clinical trial eligibility screening.
