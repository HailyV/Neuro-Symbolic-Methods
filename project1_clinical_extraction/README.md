# Project 1 – Clinical Dialogue Extraction using LLMs

This project replicates an AI backed approach to extract **structured medical information** from doctor–patient dialogues in the **MTS-Dialog dataset**.  
It demonstrates how **large language models (LLMs)** and **semantic extraction techniques** can automate entity recognition and data structuring for biomedical analysis.

---

## Overview

The pipeline uses `semlib`-style prompting and the OpenAI API to parse unstructured conversation data into structured JSON containing the following fields:

| **Field Name**       | **Description**                                                                 |
|-----------------------|---------------------------------------------------------------------------------|
| `chief_complaint`     | The patient’s primary reason for visiting the doctor, typically describing symptoms or health concerns. |
| `family_illnesses`    | A list of hereditary or family-related medical conditions mentioned during the conversation. |
| `medications`         | The medications currently being taken or prescribed to the patient.             |
| `small_talk`          | A Boolean value indicating whether casual or non-medical conversation occurred. |
| `doctor_advice`       | A summary of the doctor’s recommendations, treatment plans, or follow-up instructions. |

---

## Installation and Setup

### Clone this project

```bash
git clone https://github.com/HailyV/Neuro-Symbolic-Methods
cd Neuro-Symbolic-Methods/project1_clinical_extraction

conda create -n mts_extraction python=3.10
conda activate mts_extraction
pip install -r requirements.txt

export OPENAI_API_KEY="your_api_key"
mts_extraction.py
